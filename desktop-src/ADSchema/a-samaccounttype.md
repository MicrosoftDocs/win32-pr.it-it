---
title: Attributo SAM-account-type
description: Questo attributo contiene informazioni su ogni oggetto tipo di conto.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo SAM-account-type
- Schema AD dell'attributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965196"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="fd5b9-105">Attributo SAM-account-type</span><span class="sxs-lookup"><span data-stu-id="fd5b9-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="fd5b9-106">Questo attributo contiene informazioni su ogni oggetto tipo di conto.</span><span class="sxs-lookup"><span data-stu-id="fd5b9-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="fd5b9-107">È possibile enumerare un elenco di tipi di conto oppure usare l'API informazioni di visualizzazione per creare un elenco.</span><span class="sxs-lookup"><span data-stu-id="fd5b9-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="fd5b9-108">Poiché i computer, gli account utente normali e gli account attendibili possono anche essere enumerati come oggetti utente, i valori per questi account devono essere un intervallo contiguo.</span><span class="sxs-lookup"><span data-stu-id="fd5b9-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="fd5b9-109">I valori possibili per questo attributo sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="fd5b9-110">\_Oggetto di dominio SAM \_ 0x0</span><span class="sxs-lookup"><span data-stu-id="fd5b9-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="fd5b9-111">\_ \_ 0x10000000 oggetto gruppo Sam</span><span class="sxs-lookup"><span data-stu-id="fd5b9-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="fd5b9-112">\_ \_ \_ 0x10000001 oggetto gruppo non di sicurezza Sam \_</span><span class="sxs-lookup"><span data-stu-id="fd5b9-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="fd5b9-113">\_Oggetto alias Sam \_ 0x20000000</span><span class="sxs-lookup"><span data-stu-id="fd5b9-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="fd5b9-114">\_Oggetto alias Sam non di \_ sicurezza \_ \_ 0x20000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="fd5b9-115">\_ \_ 0x30000000 oggetto utente Sam</span><span class="sxs-lookup"><span data-stu-id="fd5b9-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="fd5b9-116">\_ \_ Account utente normale Sam \_ 0x30000000</span><span class="sxs-lookup"><span data-stu-id="fd5b9-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="fd5b9-117">\_Account del computer Sam \_ 0x30000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="fd5b9-118">\_Account attendibile Sam \_ 0x30000002</span><span class="sxs-lookup"><span data-stu-id="fd5b9-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="fd5b9-119">\_ \_ 0x40000000 gruppo Basic App Sam \_</span><span class="sxs-lookup"><span data-stu-id="fd5b9-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="fd5b9-120">\_ \_ 0x40000001 gruppo di query app Sam \_</span><span class="sxs-lookup"><span data-stu-id="fd5b9-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="fd5b9-121">\_Tipo di account SAM \_ \_ Max 0x7FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="fd5b9-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="fd5b9-122">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-122">Entry</span></span> | <span data-ttu-id="fd5b9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fd5b9-124">CN</span><span class="sxs-lookup"><span data-stu-id="fd5b9-124">CN</span></span>                | <span data-ttu-id="fd5b9-125">Tipo di account SAM</span><span class="sxs-lookup"><span data-stu-id="fd5b9-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="fd5b9-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fd5b9-126">Ldap-Display-Name</span></span> | <span data-ttu-id="fd5b9-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="fd5b9-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="fd5b9-128">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fd5b9-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="fd5b9-129">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-129">Update Privilege</span></span>  | <span data-ttu-id="fd5b9-130">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fd5b9-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="fd5b9-131">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-131">Update Frequency</span></span>  | <span data-ttu-id="fd5b9-132">Questa impostazione viene impostata dal sistema operativo quando viene creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd5b9-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="fd5b9-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-133">Attribute-Id</span></span>      | <span data-ttu-id="fd5b9-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="fd5b9-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="fd5b9-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fd5b9-135">System-Id-Guid</span></span>    | <span data-ttu-id="fd5b9-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="fd5b9-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="fd5b9-137">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd5b9-137">Syntax</span></span>            | [<span data-ttu-id="fd5b9-138">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="fd5b9-139">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fd5b9-139">Implementations</span></span>

-   [<span data-ttu-id="fd5b9-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fd5b9-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fd5b9-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fd5b9-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fd5b9-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fd5b9-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fd5b9-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd5b9-146">Windows 2000 Server</span></span>



| <span data-ttu-id="fd5b9-147">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-147">Entry</span></span> | <span data-ttu-id="fd5b9-148">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-149">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-151">System-Only</span></span>            | <span data-ttu-id="fd5b9-152">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-152">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-153">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-153">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-154">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-154">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-155">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-155">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-156">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-156">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-157">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-157">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-158">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-158">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-159">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-160">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-163">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-165">System-Flags</span></span>           | <span data-ttu-id="fd5b9-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-167">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-167">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-168">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fd5b9-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd5b9-169">Windows Server 2003</span></span>



| <span data-ttu-id="fd5b9-170">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-170">Entry</span></span> | <span data-ttu-id="fd5b9-171">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-172">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-174">System-Only</span></span>            | <span data-ttu-id="fd5b9-175">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-175">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-176">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-176">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-177">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-177">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-178">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-178">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-179">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-179">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-180">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-180">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-181">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-181">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-182">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-183">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-186">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-188">System-Flags</span></span>           | <span data-ttu-id="fd5b9-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-190">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-190">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-191">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fd5b9-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fd5b9-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fd5b9-193">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-193">Entry</span></span> | <span data-ttu-id="fd5b9-194">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-195">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-197">System-Only</span></span>            | <span data-ttu-id="fd5b9-198">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-198">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-199">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-199">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-200">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-200">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-201">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-201">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-202">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-202">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-203">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-203">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-204">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-204">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-205">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-206">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-209">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-211">System-Flags</span></span>           | <span data-ttu-id="fd5b9-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-213">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-213">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-214">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fd5b9-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd5b9-215">Windows Server 2008</span></span>



| <span data-ttu-id="fd5b9-216">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-216">Entry</span></span> | <span data-ttu-id="fd5b9-217">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-218">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-220">System-Only</span></span>            | <span data-ttu-id="fd5b9-221">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-221">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-222">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-222">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-223">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-223">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-224">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-224">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-225">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-225">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-226">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-226">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-227">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-227">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-228">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-229">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-232">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-234">System-Flags</span></span>           | <span data-ttu-id="fd5b9-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-236">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-236">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-237">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fd5b9-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd5b9-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fd5b9-239">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-239">Entry</span></span> | <span data-ttu-id="fd5b9-240">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-241">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-243">System-Only</span></span>            | <span data-ttu-id="fd5b9-244">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-244">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-245">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-245">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-246">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-246">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-247">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-247">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-248">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-248">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-249">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-249">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-250">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-250">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-251">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-252">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-255">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-257">System-Flags</span></span>           | <span data-ttu-id="fd5b9-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-259">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-260">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fd5b9-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-261">Windows Server 2012</span></span>



| <span data-ttu-id="fd5b9-262">Voce</span><span class="sxs-lookup"><span data-stu-id="fd5b9-262">Entry</span></span> | <span data-ttu-id="fd5b9-263">Valore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd5b9-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd5b9-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd5b9-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd5b9-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd5b9-266">System-Only</span></span>            | <span data-ttu-id="fd5b9-267">Falso</span><span class="sxs-lookup"><span data-stu-id="fd5b9-267">False</span></span>                                                        |
| <span data-ttu-id="fd5b9-268">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd5b9-268">Is-Single-Valued</span></span>       | <span data-ttu-id="fd5b9-269">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-269">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-270">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd5b9-270">Is Indexed</span></span>             | <span data-ttu-id="fd5b9-271">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-271">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-272">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd5b9-272">In Global Catalog</span></span>      | <span data-ttu-id="fd5b9-273">Vero</span><span class="sxs-lookup"><span data-stu-id="fd5b9-273">True</span></span>                                                         |
| <span data-ttu-id="fd5b9-274">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd5b9-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd5b9-275">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd5b9-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd5b9-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd5b9-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd5b9-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd5b9-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-278">Search-Flags</span></span>           | <span data-ttu-id="fd5b9-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd5b9-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="fd5b9-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd5b9-280">System-Flags</span></span>           | <span data-ttu-id="fd5b9-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fd5b9-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="fd5b9-282">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd5b9-282">Classes used in</span></span>        | [<span data-ttu-id="fd5b9-283">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="fd5b9-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





