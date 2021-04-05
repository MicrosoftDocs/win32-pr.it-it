---
title: Installare l'attributo a livello di interfaccia utente
description: Questo attributo contiene informazioni per il tipo (livello) di installazione usato per l'interfaccia utente.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Installare lo schema AD dell'attributo a livello di interfaccia utente
- Schema AD dell'attributo installUiLevel
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965090"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="4976f-105">Installare l'attributo a livello di interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4976f-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="4976f-106">Questo attributo contiene informazioni per il tipo (livello) di installazione usato per l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4976f-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="4976f-107">I livelli di installazione possibili sono i seguenti: 2 INSTALLUILEVEL \_ None (installazione invisibile all'utente) 3 INSTALLUILEVEL \_ Basic (installazione semplice con gestione degli errori) 4 INSTALLUILEVEL \_ ridotta (interfaccia utente creata, finestre di dialogo della procedura guidata non rilevate) 5 INSTALLUILEVEL \_ completa (interfaccia utente creata con procedure guidate, stato, errori)</span><span class="sxs-lookup"><span data-stu-id="4976f-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="4976f-108">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-108">Entry</span></span> | <span data-ttu-id="4976f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4976f-110">CN</span><span class="sxs-lookup"><span data-stu-id="4976f-110">CN</span></span>                | <span data-ttu-id="4976f-111">Installare-a livello di interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4976f-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="4976f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4976f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="4976f-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="4976f-113">installUiLevel</span></span>                       |
| <span data-ttu-id="4976f-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4976f-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="4976f-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4976f-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4976f-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4976f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4976f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-117">Attribute-Id</span></span>      | <span data-ttu-id="4976f-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="4976f-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="4976f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4976f-119">System-Id-Guid</span></span>    | <span data-ttu-id="4976f-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4976f-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="4976f-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4976f-121">Syntax</span></span>            | [<span data-ttu-id="4976f-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="4976f-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="4976f-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4976f-123">Implementations</span></span>

-   [<span data-ttu-id="4976f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4976f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4976f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4976f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4976f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4976f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4976f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4976f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4976f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4976f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4976f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4976f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4976f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4976f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4976f-131">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-131">Entry</span></span> | <span data-ttu-id="4976f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-135">System-Only</span></span>            | <span data-ttu-id="4976f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-136">False</span></span>                                                            |
| <span data-ttu-id="4976f-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-138">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-138">True</span></span>                                                             |
| <span data-ttu-id="4976f-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-139">Is Indexed</span></span>             | <span data-ttu-id="4976f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-140">False</span></span>                                                            |
| <span data-ttu-id="4976f-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-141">In Global Catalog</span></span>      | <span data-ttu-id="4976f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-142">False</span></span>                                                            |
| <span data-ttu-id="4976f-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-147">Search-Flags</span></span>           | <span data-ttu-id="4976f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-149">System-Flags</span></span>           | <span data-ttu-id="4976f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-151">Classes used in</span></span>        | [<span data-ttu-id="4976f-152">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4976f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4976f-153">Windows Server 2003</span></span>



| <span data-ttu-id="4976f-154">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-154">Entry</span></span> | <span data-ttu-id="4976f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-158">System-Only</span></span>            | <span data-ttu-id="4976f-159">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-159">False</span></span>                                                            |
| <span data-ttu-id="4976f-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-161">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-161">True</span></span>                                                             |
| <span data-ttu-id="4976f-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-162">Is Indexed</span></span>             | <span data-ttu-id="4976f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-163">False</span></span>                                                            |
| <span data-ttu-id="4976f-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-164">In Global Catalog</span></span>      | <span data-ttu-id="4976f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-165">False</span></span>                                                            |
| <span data-ttu-id="4976f-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-170">Search-Flags</span></span>           | <span data-ttu-id="4976f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-172">System-Flags</span></span>           | <span data-ttu-id="4976f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-174">Classes used in</span></span>        | [<span data-ttu-id="4976f-175">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4976f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4976f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4976f-177">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-177">Entry</span></span> | <span data-ttu-id="4976f-178">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-181">System-Only</span></span>            | <span data-ttu-id="4976f-182">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-182">False</span></span>                                                            |
| <span data-ttu-id="4976f-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-184">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-184">True</span></span>                                                             |
| <span data-ttu-id="4976f-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-185">Is Indexed</span></span>             | <span data-ttu-id="4976f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-186">False</span></span>                                                            |
| <span data-ttu-id="4976f-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-187">In Global Catalog</span></span>      | <span data-ttu-id="4976f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-188">False</span></span>                                                            |
| <span data-ttu-id="4976f-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-193">Search-Flags</span></span>           | <span data-ttu-id="4976f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-195">System-Flags</span></span>           | <span data-ttu-id="4976f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-197">Classes used in</span></span>        | [<span data-ttu-id="4976f-198">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4976f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4976f-199">Windows Server 2008</span></span>



| <span data-ttu-id="4976f-200">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-200">Entry</span></span> | <span data-ttu-id="4976f-201">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-204">System-Only</span></span>            | <span data-ttu-id="4976f-205">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-205">False</span></span>                                                            |
| <span data-ttu-id="4976f-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-207">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-207">True</span></span>                                                             |
| <span data-ttu-id="4976f-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-208">Is Indexed</span></span>             | <span data-ttu-id="4976f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-209">False</span></span>                                                            |
| <span data-ttu-id="4976f-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-210">In Global Catalog</span></span>      | <span data-ttu-id="4976f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-211">False</span></span>                                                            |
| <span data-ttu-id="4976f-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-216">Search-Flags</span></span>           | <span data-ttu-id="4976f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-218">System-Flags</span></span>           | <span data-ttu-id="4976f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-220">Classes used in</span></span>        | [<span data-ttu-id="4976f-221">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4976f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4976f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4976f-223">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-223">Entry</span></span> | <span data-ttu-id="4976f-224">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-227">System-Only</span></span>            | <span data-ttu-id="4976f-228">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-228">False</span></span>                                                            |
| <span data-ttu-id="4976f-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-230">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-230">True</span></span>                                                             |
| <span data-ttu-id="4976f-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-231">Is Indexed</span></span>             | <span data-ttu-id="4976f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-232">False</span></span>                                                            |
| <span data-ttu-id="4976f-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-233">In Global Catalog</span></span>      | <span data-ttu-id="4976f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-234">False</span></span>                                                            |
| <span data-ttu-id="4976f-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-239">Search-Flags</span></span>           | <span data-ttu-id="4976f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-241">System-Flags</span></span>           | <span data-ttu-id="4976f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-243">Classes used in</span></span>        | [<span data-ttu-id="4976f-244">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4976f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4976f-245">Windows Server 2012</span></span>



| <span data-ttu-id="4976f-246">Voce</span><span class="sxs-lookup"><span data-stu-id="4976f-246">Entry</span></span> | <span data-ttu-id="4976f-247">Valore</span><span class="sxs-lookup"><span data-stu-id="4976f-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4976f-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4976f-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4976f-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="4976f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4976f-250">System-Only</span></span>            | <span data-ttu-id="4976f-251">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-251">False</span></span>                                                            |
| <span data-ttu-id="4976f-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4976f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4976f-253">Vero</span><span class="sxs-lookup"><span data-stu-id="4976f-253">True</span></span>                                                             |
| <span data-ttu-id="4976f-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4976f-254">Is Indexed</span></span>             | <span data-ttu-id="4976f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-255">False</span></span>                                                            |
| <span data-ttu-id="4976f-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4976f-256">In Global Catalog</span></span>      | <span data-ttu-id="4976f-257">Falso</span><span class="sxs-lookup"><span data-stu-id="4976f-257">False</span></span>                                                            |
| <span data-ttu-id="4976f-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4976f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4976f-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4976f-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="4976f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4976f-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4976f-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="4976f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-262">Search-Flags</span></span>           | <span data-ttu-id="4976f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4976f-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="4976f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4976f-264">System-Flags</span></span>           | <span data-ttu-id="4976f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4976f-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="4976f-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4976f-266">Classes used in</span></span>        | [<span data-ttu-id="4976f-267">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="4976f-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





