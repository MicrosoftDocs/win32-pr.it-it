---
title: attributo ms-TS-profile-path
description: Percorso profilo Servizi terminal specifica un percorso del profilo di roaming o obbligatorio da utilizzare quando l'utente accede al server terminal. Il percorso del profilo si trova nel formato del percorso di rete seguente \\ \\ NomeServer \\ ProfilesFolderName \\ nomeutente.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- Schema di AD di attributo ms-TS-profile-path
- Schema AD dell'attributo msTSProfilePath
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965226"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="3f64c-106">attributo ms-TS-profile-path</span><span class="sxs-lookup"><span data-stu-id="3f64c-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="3f64c-107">Percorso profilo Servizi terminal specifica un percorso del profilo di roaming o obbligatorio da utilizzare quando l'utente accede al server terminal.</span><span class="sxs-lookup"><span data-stu-id="3f64c-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="3f64c-108">Il percorso del profilo si trova nel seguente formato di percorso di rete: **\\\\** _nomeserver_ *_\\_* _ProfilesFolderName_ *_\\_* _nomeutente_.</span><span class="sxs-lookup"><span data-stu-id="3f64c-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="3f64c-109">Voce</span><span class="sxs-lookup"><span data-stu-id="3f64c-109">Entry</span></span> | <span data-ttu-id="3f64c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3f64c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3f64c-111">CN</span><span class="sxs-lookup"><span data-stu-id="3f64c-111">CN</span></span>                | <span data-ttu-id="3f64c-112">MS-TS-profile-path</span><span class="sxs-lookup"><span data-stu-id="3f64c-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="3f64c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3f64c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3f64c-114">msTSProfilePath</span><span class="sxs-lookup"><span data-stu-id="3f64c-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="3f64c-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3f64c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3f64c-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3f64c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3f64c-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3f64c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3f64c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f64c-118">Attribute-Id</span></span>      | <span data-ttu-id="3f64c-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="3f64c-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="3f64c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f64c-120">System-Id-Guid</span></span>    | <span data-ttu-id="3f64c-121">e65c30db-316c-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="3f64c-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="3f64c-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f64c-122">Syntax</span></span>            | [<span data-ttu-id="3f64c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3f64c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3f64c-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3f64c-124">Implementations</span></span>

-   [<span data-ttu-id="3f64c-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f64c-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f64c-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f64c-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f64c-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f64c-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3f64c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f64c-128">Windows Server 2008</span></span>



| <span data-ttu-id="3f64c-129">Voce</span><span class="sxs-lookup"><span data-stu-id="3f64c-129">Entry</span></span> | <span data-ttu-id="3f64c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3f64c-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3f64c-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3f64c-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f64c-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f64c-133">System-Only</span></span>            | <span data-ttu-id="3f64c-134">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-134">False</span></span>                             |
| <span data-ttu-id="3f64c-135">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3f64c-135">Is-Single-Valued</span></span>       | <span data-ttu-id="3f64c-136">Vero</span><span class="sxs-lookup"><span data-stu-id="3f64c-136">True</span></span>                              |
| <span data-ttu-id="3f64c-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3f64c-137">Is Indexed</span></span>             | <span data-ttu-id="3f64c-138">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-138">False</span></span>                             |
| <span data-ttu-id="3f64c-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3f64c-139">In Global Catalog</span></span>      | <span data-ttu-id="3f64c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-140">False</span></span>                             |
| <span data-ttu-id="3f64c-141">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3f64c-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f64c-142">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3f64c-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3f64c-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f64c-143">Range-Lower</span></span>            | <span data-ttu-id="3f64c-144">0</span><span class="sxs-lookup"><span data-stu-id="3f64c-144">0</span></span>                                 |
| <span data-ttu-id="3f64c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f64c-145">Range-Upper</span></span>            | <span data-ttu-id="3f64c-146">32767</span><span class="sxs-lookup"><span data-stu-id="3f64c-146">32767</span></span>                             |
| <span data-ttu-id="3f64c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-147">Search-Flags</span></span>           | <span data-ttu-id="3f64c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f64c-148">0x00000000</span></span>                        |
| <span data-ttu-id="3f64c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-149">System-Flags</span></span>           | <span data-ttu-id="3f64c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f64c-150">0x00000010</span></span>                        |
| <span data-ttu-id="3f64c-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3f64c-151">Classes used in</span></span>        | [<span data-ttu-id="3f64c-152">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3f64c-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f64c-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f64c-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f64c-154">Voce</span><span class="sxs-lookup"><span data-stu-id="3f64c-154">Entry</span></span> | <span data-ttu-id="3f64c-155">Valore</span><span class="sxs-lookup"><span data-stu-id="3f64c-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3f64c-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3f64c-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f64c-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f64c-158">System-Only</span></span>            | <span data-ttu-id="3f64c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-159">False</span></span>                             |
| <span data-ttu-id="3f64c-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3f64c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3f64c-161">Vero</span><span class="sxs-lookup"><span data-stu-id="3f64c-161">True</span></span>                              |
| <span data-ttu-id="3f64c-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3f64c-162">Is Indexed</span></span>             | <span data-ttu-id="3f64c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-163">False</span></span>                             |
| <span data-ttu-id="3f64c-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3f64c-164">In Global Catalog</span></span>      | <span data-ttu-id="3f64c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-165">False</span></span>                             |
| <span data-ttu-id="3f64c-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3f64c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f64c-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3f64c-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3f64c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f64c-168">Range-Lower</span></span>            | <span data-ttu-id="3f64c-169">0</span><span class="sxs-lookup"><span data-stu-id="3f64c-169">0</span></span>                                 |
| <span data-ttu-id="3f64c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f64c-170">Range-Upper</span></span>            | <span data-ttu-id="3f64c-171">32767</span><span class="sxs-lookup"><span data-stu-id="3f64c-171">32767</span></span>                             |
| <span data-ttu-id="3f64c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-172">Search-Flags</span></span>           | <span data-ttu-id="3f64c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f64c-173">0x00000000</span></span>                        |
| <span data-ttu-id="3f64c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-174">System-Flags</span></span>           | <span data-ttu-id="3f64c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f64c-175">0x00000010</span></span>                        |
| <span data-ttu-id="3f64c-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3f64c-176">Classes used in</span></span>        | [<span data-ttu-id="3f64c-177">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3f64c-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f64c-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f64c-178">Windows Server 2012</span></span>



| <span data-ttu-id="3f64c-179">Voce</span><span class="sxs-lookup"><span data-stu-id="3f64c-179">Entry</span></span> | <span data-ttu-id="3f64c-180">Valore</span><span class="sxs-lookup"><span data-stu-id="3f64c-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3f64c-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3f64c-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f64c-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3f64c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f64c-183">System-Only</span></span>            | <span data-ttu-id="3f64c-184">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-184">False</span></span>                             |
| <span data-ttu-id="3f64c-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3f64c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3f64c-186">Vero</span><span class="sxs-lookup"><span data-stu-id="3f64c-186">True</span></span>                              |
| <span data-ttu-id="3f64c-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3f64c-187">Is Indexed</span></span>             | <span data-ttu-id="3f64c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-188">False</span></span>                             |
| <span data-ttu-id="3f64c-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3f64c-189">In Global Catalog</span></span>      | <span data-ttu-id="3f64c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3f64c-190">False</span></span>                             |
| <span data-ttu-id="3f64c-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3f64c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f64c-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3f64c-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3f64c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f64c-193">Range-Lower</span></span>            | <span data-ttu-id="3f64c-194">0</span><span class="sxs-lookup"><span data-stu-id="3f64c-194">0</span></span>                                 |
| <span data-ttu-id="3f64c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f64c-195">Range-Upper</span></span>            | <span data-ttu-id="3f64c-196">32767</span><span class="sxs-lookup"><span data-stu-id="3f64c-196">32767</span></span>                             |
| <span data-ttu-id="3f64c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-197">Search-Flags</span></span>           | <span data-ttu-id="3f64c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f64c-198">0x00000000</span></span>                        |
| <span data-ttu-id="3f64c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f64c-199">System-Flags</span></span>           | <span data-ttu-id="3f64c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f64c-200">0x00000010</span></span>                        |
| <span data-ttu-id="3f64c-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3f64c-201">Classes used in</span></span>        | [<span data-ttu-id="3f64c-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3f64c-202">**User**</span></span>](c-user.md)<br/> |



 

 





