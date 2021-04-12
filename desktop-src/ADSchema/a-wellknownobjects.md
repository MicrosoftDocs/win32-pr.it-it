---
title: Attributo well-known-Objects
description: Questo attributo contiene un elenco di contenitori di oggetti noti per GUID e nome distinto.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo well-known-Objects
- Schema AD dell'attributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480200"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="56d05-105">Attributo well-known-Objects</span><span class="sxs-lookup"><span data-stu-id="56d05-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="56d05-106">Questo attributo contiene un elenco di contenitori di oggetti noti per GUID e nome distinto.</span><span class="sxs-lookup"><span data-stu-id="56d05-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="56d05-107">Gli oggetti noti sono contenitori di sistema.</span><span class="sxs-lookup"><span data-stu-id="56d05-107">The well-known objects are system containers.</span></span> <span data-ttu-id="56d05-108">Queste informazioni vengono utilizzate per recuperare un oggetto dopo che è stato spostato utilizzando solo il GUID e il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="56d05-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="56d05-109">Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente la parte del nome distinto dei valori degli oggetti noti che fanno riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56d05-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="56d05-110">Il file ntdsapi. h contiene le seguenti definizioni, che possono essere usate per recuperare un oggetto (i GUID associati a questi oggetti sono contenuti in ntdsapi. h):</span><span class="sxs-lookup"><span data-stu-id="56d05-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="56d05-111">\_contenitore utenti \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-112">\_contenitore di calcolo \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-113">\_contenitore di sistemi GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-114">\_contenitore controller di dominio GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-115">\_contenitore infrastruttura \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-116">\_ \_ contenitore oggetti eliminati \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-117">GUID \_ LOSTANDFOUND \_ contenitore \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-118">GUID \_ FOREIGNSECURITYPRINCIPALS \_ contenitore \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-119">\_contenitore di dati del programma GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-120">\_contenitore di \_ dati del programma Microsoft GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="56d05-121">\_ \_ contenitore quote NTDS GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="56d05-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="56d05-122">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-122">Entry</span></span> | <span data-ttu-id="56d05-123">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="56d05-124">CN</span><span class="sxs-lookup"><span data-stu-id="56d05-124">CN</span></span>                | <span data-ttu-id="56d05-125">Oggetti noti</span><span class="sxs-lookup"><span data-stu-id="56d05-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="56d05-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="56d05-126">Ldap-Display-Name</span></span> | <span data-ttu-id="56d05-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="56d05-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="56d05-128">Dimensione</span><span class="sxs-lookup"><span data-stu-id="56d05-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="56d05-129">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="56d05-129">Update Privilege</span></span>  | <span data-ttu-id="56d05-130">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="56d05-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="56d05-131">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="56d05-131">Update Frequency</span></span>  | <span data-ttu-id="56d05-132">Ogni volta che uno dei contenitori di sistema viene spostato.</span><span class="sxs-lookup"><span data-stu-id="56d05-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="56d05-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-133">Attribute-Id</span></span>      | <span data-ttu-id="56d05-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="56d05-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="56d05-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="56d05-135">System-Id-Guid</span></span>    | <span data-ttu-id="56d05-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="56d05-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="56d05-137">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56d05-137">Syntax</span></span>            | [<span data-ttu-id="56d05-138">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="56d05-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="56d05-139">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="56d05-139">Implementations</span></span>

-   [<span data-ttu-id="56d05-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56d05-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56d05-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56d05-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56d05-142">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="56d05-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="56d05-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56d05-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56d05-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56d05-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56d05-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56d05-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56d05-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56d05-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56d05-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56d05-147">Windows 2000 Server</span></span>



| <span data-ttu-id="56d05-148">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-148">Entry</span></span> | <span data-ttu-id="56d05-149">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-150">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-152">System-Only</span></span>            | <span data-ttu-id="56d05-153">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-153">True</span></span>                            |
| <span data-ttu-id="56d05-154">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-154">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-155">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-155">False</span></span>                           |
| <span data-ttu-id="56d05-156">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-156">Is Indexed</span></span>             | <span data-ttu-id="56d05-157">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-157">False</span></span>                           |
| <span data-ttu-id="56d05-158">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-158">In Global Catalog</span></span>      | <span data-ttu-id="56d05-159">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-159">True</span></span>                            |
| <span data-ttu-id="56d05-160">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-161">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56d05-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56d05-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-164">Search-Flags</span></span>           | <span data-ttu-id="56d05-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-165">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-166">System-Flags</span></span>           | <span data-ttu-id="56d05-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-167">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-168">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-168">Classes used in</span></span>        | [<span data-ttu-id="56d05-169">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56d05-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56d05-170">Windows Server 2003</span></span>



| <span data-ttu-id="56d05-171">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-171">Entry</span></span> | <span data-ttu-id="56d05-172">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-173">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-175">System-Only</span></span>            | <span data-ttu-id="56d05-176">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-176">True</span></span>                            |
| <span data-ttu-id="56d05-177">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-177">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-178">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-178">False</span></span>                           |
| <span data-ttu-id="56d05-179">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-179">Is Indexed</span></span>             | <span data-ttu-id="56d05-180">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-180">False</span></span>                           |
| <span data-ttu-id="56d05-181">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-181">In Global Catalog</span></span>      | <span data-ttu-id="56d05-182">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-182">True</span></span>                            |
| <span data-ttu-id="56d05-183">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-184">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-185">Range-Lower</span></span>            | <span data-ttu-id="56d05-186">16</span><span class="sxs-lookup"><span data-stu-id="56d05-186">16</span></span>                              |
| <span data-ttu-id="56d05-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-187">Range-Upper</span></span>            | <span data-ttu-id="56d05-188">16</span><span class="sxs-lookup"><span data-stu-id="56d05-188">16</span></span>                              |
| <span data-ttu-id="56d05-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-189">Search-Flags</span></span>           | <span data-ttu-id="56d05-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-190">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-191">System-Flags</span></span>           | <span data-ttu-id="56d05-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-192">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-193">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-193">Classes used in</span></span>        | [<span data-ttu-id="56d05-194">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="56d05-195">ADAM</span><span class="sxs-lookup"><span data-stu-id="56d05-195">ADAM</span></span>



| <span data-ttu-id="56d05-196">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-196">Entry</span></span> | <span data-ttu-id="56d05-197">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-198">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-200">System-Only</span></span>            | <span data-ttu-id="56d05-201">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-201">True</span></span>                            |
| <span data-ttu-id="56d05-202">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-202">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-203">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-203">False</span></span>                           |
| <span data-ttu-id="56d05-204">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-204">Is Indexed</span></span>             | <span data-ttu-id="56d05-205">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-205">False</span></span>                           |
| <span data-ttu-id="56d05-206">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-206">In Global Catalog</span></span>      | <span data-ttu-id="56d05-207">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-207">True</span></span>                            |
| <span data-ttu-id="56d05-208">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-209">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-210">Range-Lower</span></span>            | <span data-ttu-id="56d05-211">16</span><span class="sxs-lookup"><span data-stu-id="56d05-211">16</span></span>                              |
| <span data-ttu-id="56d05-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-212">Range-Upper</span></span>            | <span data-ttu-id="56d05-213">16</span><span class="sxs-lookup"><span data-stu-id="56d05-213">16</span></span>                              |
| <span data-ttu-id="56d05-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-214">Search-Flags</span></span>           | <span data-ttu-id="56d05-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-215">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-216">System-Flags</span></span>           | <span data-ttu-id="56d05-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-217">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-218">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-218">Classes used in</span></span>        | [<span data-ttu-id="56d05-219">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56d05-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56d05-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56d05-221">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-221">Entry</span></span> | <span data-ttu-id="56d05-222">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-223">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-225">System-Only</span></span>            | <span data-ttu-id="56d05-226">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-226">True</span></span>                            |
| <span data-ttu-id="56d05-227">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-227">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-228">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-228">False</span></span>                           |
| <span data-ttu-id="56d05-229">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-229">Is Indexed</span></span>             | <span data-ttu-id="56d05-230">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-230">False</span></span>                           |
| <span data-ttu-id="56d05-231">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-231">In Global Catalog</span></span>      | <span data-ttu-id="56d05-232">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-232">True</span></span>                            |
| <span data-ttu-id="56d05-233">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-234">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-235">Range-Lower</span></span>            | <span data-ttu-id="56d05-236">16</span><span class="sxs-lookup"><span data-stu-id="56d05-236">16</span></span>                              |
| <span data-ttu-id="56d05-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-237">Range-Upper</span></span>            | <span data-ttu-id="56d05-238">16</span><span class="sxs-lookup"><span data-stu-id="56d05-238">16</span></span>                              |
| <span data-ttu-id="56d05-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-239">Search-Flags</span></span>           | <span data-ttu-id="56d05-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-240">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-241">System-Flags</span></span>           | <span data-ttu-id="56d05-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-242">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-243">Classes used in</span></span>        | [<span data-ttu-id="56d05-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56d05-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56d05-245">Windows Server 2008</span></span>



| <span data-ttu-id="56d05-246">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-246">Entry</span></span> | <span data-ttu-id="56d05-247">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-250">System-Only</span></span>            | <span data-ttu-id="56d05-251">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-251">True</span></span>                            |
| <span data-ttu-id="56d05-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-252">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-253">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-253">False</span></span>                           |
| <span data-ttu-id="56d05-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-254">Is Indexed</span></span>             | <span data-ttu-id="56d05-255">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-255">False</span></span>                           |
| <span data-ttu-id="56d05-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-256">In Global Catalog</span></span>      | <span data-ttu-id="56d05-257">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-257">True</span></span>                            |
| <span data-ttu-id="56d05-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-260">Range-Lower</span></span>            | <span data-ttu-id="56d05-261">16</span><span class="sxs-lookup"><span data-stu-id="56d05-261">16</span></span>                              |
| <span data-ttu-id="56d05-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-262">Range-Upper</span></span>            | <span data-ttu-id="56d05-263">16</span><span class="sxs-lookup"><span data-stu-id="56d05-263">16</span></span>                              |
| <span data-ttu-id="56d05-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-264">Search-Flags</span></span>           | <span data-ttu-id="56d05-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-265">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-266">System-Flags</span></span>           | <span data-ttu-id="56d05-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-267">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-268">Classes used in</span></span>        | [<span data-ttu-id="56d05-269">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56d05-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56d05-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56d05-271">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-271">Entry</span></span> | <span data-ttu-id="56d05-272">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-275">System-Only</span></span>            | <span data-ttu-id="56d05-276">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-276">True</span></span>                            |
| <span data-ttu-id="56d05-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-277">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-278">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-278">False</span></span>                           |
| <span data-ttu-id="56d05-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-279">Is Indexed</span></span>             | <span data-ttu-id="56d05-280">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-280">False</span></span>                           |
| <span data-ttu-id="56d05-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-281">In Global Catalog</span></span>      | <span data-ttu-id="56d05-282">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-282">True</span></span>                            |
| <span data-ttu-id="56d05-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-285">Range-Lower</span></span>            | <span data-ttu-id="56d05-286">16</span><span class="sxs-lookup"><span data-stu-id="56d05-286">16</span></span>                              |
| <span data-ttu-id="56d05-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-287">Range-Upper</span></span>            | <span data-ttu-id="56d05-288">16</span><span class="sxs-lookup"><span data-stu-id="56d05-288">16</span></span>                              |
| <span data-ttu-id="56d05-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-289">Search-Flags</span></span>           | <span data-ttu-id="56d05-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-290">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-291">System-Flags</span></span>           | <span data-ttu-id="56d05-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-292">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-293">Classes used in</span></span>        | [<span data-ttu-id="56d05-294">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56d05-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56d05-295">Windows Server 2012</span></span>



| <span data-ttu-id="56d05-296">Voce</span><span class="sxs-lookup"><span data-stu-id="56d05-296">Entry</span></span> | <span data-ttu-id="56d05-297">Valore</span><span class="sxs-lookup"><span data-stu-id="56d05-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56d05-298">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="56d05-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56d05-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="56d05-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="56d05-300">System-Only</span></span>            | <span data-ttu-id="56d05-301">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-301">True</span></span>                            |
| <span data-ttu-id="56d05-302">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="56d05-302">Is-Single-Valued</span></span>       | <span data-ttu-id="56d05-303">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-303">False</span></span>                           |
| <span data-ttu-id="56d05-304">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="56d05-304">Is Indexed</span></span>             | <span data-ttu-id="56d05-305">Falso</span><span class="sxs-lookup"><span data-stu-id="56d05-305">False</span></span>                           |
| <span data-ttu-id="56d05-306">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="56d05-306">In Global Catalog</span></span>      | <span data-ttu-id="56d05-307">Vero</span><span class="sxs-lookup"><span data-stu-id="56d05-307">True</span></span>                            |
| <span data-ttu-id="56d05-308">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="56d05-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="56d05-309">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="56d05-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56d05-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56d05-310">Range-Lower</span></span>            | <span data-ttu-id="56d05-311">16</span><span class="sxs-lookup"><span data-stu-id="56d05-311">16</span></span>                              |
| <span data-ttu-id="56d05-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56d05-312">Range-Upper</span></span>            | <span data-ttu-id="56d05-313">16</span><span class="sxs-lookup"><span data-stu-id="56d05-313">16</span></span>                              |
| <span data-ttu-id="56d05-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-314">Search-Flags</span></span>           | <span data-ttu-id="56d05-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56d05-315">0x00000000</span></span>                      |
| <span data-ttu-id="56d05-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56d05-316">System-Flags</span></span>           | <span data-ttu-id="56d05-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="56d05-317">0x00000012</span></span>                      |
| <span data-ttu-id="56d05-318">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="56d05-318">Classes used in</span></span>        | [<span data-ttu-id="56d05-319">**In alto**</span><span class="sxs-lookup"><span data-stu-id="56d05-319">**Top**</span></span>](c-top.md)<br/> |



 

 





