---
title: Attributo DS-UI-admin-Notification
description: Si tratta di un elenco di GUID di oggetti COM che supportano un'interfaccia di callback che DSAdmin chiama quando si verifica un'azione su un oggetto tramite l'interfaccia utente.
ms.assetid: 4845c221-087f-49f5-a95d-71f58a4e8819
ms.tgt_platform: multiple
keywords:
- DS-UI-admin-schema AD dell'attributo di notifica
- Schema AD dell'attributo dSUIAdminNotification
topic_type:
- apiref
api_name:
- DS-UI-Admin-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7082d7a8fd751fa001ac796d2a86b60a28463e8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302931"
---
# <a name="ds-ui-admin-notification-attribute"></a><span data-ttu-id="5c950-105">Attributo DS-UI-admin-Notification</span><span class="sxs-lookup"><span data-stu-id="5c950-105">DS-UI-Admin-Notification attribute</span></span>

<span data-ttu-id="5c950-106">Si tratta di un elenco di GUID di oggetti COM che supportano un'interfaccia di callback che DSAdmin chiama quando si verifica un'azione su un oggetto tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5c950-106">This is a list of the GUIDs of COM objects that support a callback interface that DSAdmin calls when an action has occurred on an object through the UI.</span></span>



| <span data-ttu-id="5c950-107">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-107">Entry</span></span> | <span data-ttu-id="5c950-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5c950-109">CN</span><span class="sxs-lookup"><span data-stu-id="5c950-109">CN</span></span>                | <span data-ttu-id="5c950-110">DS-UI-admin-notifica</span><span class="sxs-lookup"><span data-stu-id="5c950-110">DS-UI-Admin-Notification</span></span>                    |
| <span data-ttu-id="5c950-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5c950-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5c950-112">dSUIAdminNotification</span><span class="sxs-lookup"><span data-stu-id="5c950-112">dSUIAdminNotification</span></span>                       |
| <span data-ttu-id="5c950-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5c950-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5c950-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5c950-114">Update Privilege</span></span>  | <span data-ttu-id="5c950-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="5c950-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="5c950-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5c950-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5c950-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-117">Attribute-Id</span></span>      | <span data-ttu-id="5c950-118">1.2.840.113556.1.4.1343</span><span class="sxs-lookup"><span data-stu-id="5c950-118">1.2.840.113556.1.4.1343</span></span>                     |
| <span data-ttu-id="5c950-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5c950-119">System-Id-Guid</span></span>    | <span data-ttu-id="5c950-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="5c950-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span></span>        |
| <span data-ttu-id="5c950-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c950-121">Syntax</span></span>            | [<span data-ttu-id="5c950-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5c950-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5c950-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5c950-123">Implementations</span></span>

-   [<span data-ttu-id="5c950-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c950-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c950-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c950-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c950-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c950-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c950-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c950-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c950-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c950-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c950-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c950-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c950-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c950-130">Windows 2000 Server</span></span>



| <span data-ttu-id="5c950-131">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-131">Entry</span></span> | <span data-ttu-id="5c950-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-135">System-Only</span></span>            | <span data-ttu-id="5c950-136">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-136">False</span></span>                                               |
| <span data-ttu-id="5c950-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-138">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-138">False</span></span>                                               |
| <span data-ttu-id="5c950-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-139">Is Indexed</span></span>             | <span data-ttu-id="5c950-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-140">False</span></span>                                               |
| <span data-ttu-id="5c950-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-141">In Global Catalog</span></span>      | <span data-ttu-id="5c950-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-142">False</span></span>                                               |
| <span data-ttu-id="5c950-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-147">Search-Flags</span></span>           | <span data-ttu-id="5c950-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-148">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-149">System-Flags</span></span>           | <span data-ttu-id="5c950-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-150">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-151">Classes used in</span></span>        | [<span data-ttu-id="5c950-152">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-152">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c950-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c950-153">Windows Server 2003</span></span>



| <span data-ttu-id="5c950-154">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-154">Entry</span></span> | <span data-ttu-id="5c950-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-158">System-Only</span></span>            | <span data-ttu-id="5c950-159">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-159">False</span></span>                                               |
| <span data-ttu-id="5c950-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-161">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-161">False</span></span>                                               |
| <span data-ttu-id="5c950-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-162">Is Indexed</span></span>             | <span data-ttu-id="5c950-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-163">False</span></span>                                               |
| <span data-ttu-id="5c950-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-164">In Global Catalog</span></span>      | <span data-ttu-id="5c950-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-165">False</span></span>                                               |
| <span data-ttu-id="5c950-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-170">Search-Flags</span></span>           | <span data-ttu-id="5c950-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-171">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-172">System-Flags</span></span>           | <span data-ttu-id="5c950-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-173">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-174">Classes used in</span></span>        | [<span data-ttu-id="5c950-175">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-175">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c950-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c950-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c950-177">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-177">Entry</span></span> | <span data-ttu-id="5c950-178">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-181">System-Only</span></span>            | <span data-ttu-id="5c950-182">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-182">False</span></span>                                               |
| <span data-ttu-id="5c950-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-184">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-184">False</span></span>                                               |
| <span data-ttu-id="5c950-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-185">Is Indexed</span></span>             | <span data-ttu-id="5c950-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-186">False</span></span>                                               |
| <span data-ttu-id="5c950-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-187">In Global Catalog</span></span>      | <span data-ttu-id="5c950-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-188">False</span></span>                                               |
| <span data-ttu-id="5c950-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-193">Search-Flags</span></span>           | <span data-ttu-id="5c950-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-194">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-195">System-Flags</span></span>           | <span data-ttu-id="5c950-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-196">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-197">Classes used in</span></span>        | [<span data-ttu-id="5c950-198">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-198">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c950-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c950-199">Windows Server 2008</span></span>



| <span data-ttu-id="5c950-200">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-200">Entry</span></span> | <span data-ttu-id="5c950-201">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-204">System-Only</span></span>            | <span data-ttu-id="5c950-205">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-205">False</span></span>                                               |
| <span data-ttu-id="5c950-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-207">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-207">False</span></span>                                               |
| <span data-ttu-id="5c950-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-208">Is Indexed</span></span>             | <span data-ttu-id="5c950-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-209">False</span></span>                                               |
| <span data-ttu-id="5c950-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-210">In Global Catalog</span></span>      | <span data-ttu-id="5c950-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-211">False</span></span>                                               |
| <span data-ttu-id="5c950-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-216">Search-Flags</span></span>           | <span data-ttu-id="5c950-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-217">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-218">System-Flags</span></span>           | <span data-ttu-id="5c950-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-219">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-220">Classes used in</span></span>        | [<span data-ttu-id="5c950-221">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-221">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c950-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c950-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c950-223">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-223">Entry</span></span> | <span data-ttu-id="5c950-224">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-227">System-Only</span></span>            | <span data-ttu-id="5c950-228">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-228">False</span></span>                                               |
| <span data-ttu-id="5c950-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-230">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-230">False</span></span>                                               |
| <span data-ttu-id="5c950-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-231">Is Indexed</span></span>             | <span data-ttu-id="5c950-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-232">False</span></span>                                               |
| <span data-ttu-id="5c950-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-233">In Global Catalog</span></span>      | <span data-ttu-id="5c950-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-234">False</span></span>                                               |
| <span data-ttu-id="5c950-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-239">Search-Flags</span></span>           | <span data-ttu-id="5c950-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-240">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-241">System-Flags</span></span>           | <span data-ttu-id="5c950-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-242">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-243">Classes used in</span></span>        | [<span data-ttu-id="5c950-244">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-244">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c950-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c950-245">Windows Server 2012</span></span>



| <span data-ttu-id="5c950-246">Voce</span><span class="sxs-lookup"><span data-stu-id="5c950-246">Entry</span></span> | <span data-ttu-id="5c950-247">Valore</span><span class="sxs-lookup"><span data-stu-id="5c950-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c950-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5c950-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c950-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5c950-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c950-250">System-Only</span></span>            | <span data-ttu-id="5c950-251">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-251">False</span></span>                                               |
| <span data-ttu-id="5c950-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5c950-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5c950-253">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-253">False</span></span>                                               |
| <span data-ttu-id="5c950-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5c950-254">Is Indexed</span></span>             | <span data-ttu-id="5c950-255">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-255">False</span></span>                                               |
| <span data-ttu-id="5c950-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5c950-256">In Global Catalog</span></span>      | <span data-ttu-id="5c950-257">Falso</span><span class="sxs-lookup"><span data-stu-id="5c950-257">False</span></span>                                               |
| <span data-ttu-id="5c950-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5c950-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c950-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5c950-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5c950-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c950-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c950-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5c950-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-262">Search-Flags</span></span>           | <span data-ttu-id="5c950-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c950-263">0x00000000</span></span>                                          |
| <span data-ttu-id="5c950-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c950-264">System-Flags</span></span>           | <span data-ttu-id="5c950-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c950-265">0x00000010</span></span>                                          |
| <span data-ttu-id="5c950-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5c950-266">Classes used in</span></span>        | [<span data-ttu-id="5c950-267">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5c950-267">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





