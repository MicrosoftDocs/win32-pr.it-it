---
title: Attributo User-Workstations
description: Contiene i nomi NetBIOS o DNS dei computer che eseguono Windows NT Workstation o Windows 2000 Professional da cui l'utente può effettuare l'accesso.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Schema AD User-Workstations attribute
- Schema AD dell'attributo userWorkstations
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875118"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="09c43-105">Attributo User-Workstations</span><span class="sxs-lookup"><span data-stu-id="09c43-105">User-Workstations attribute</span></span>

<span data-ttu-id="09c43-106">Contiene i nomi NetBIOS o DNS dei computer che eseguono Windows NT Workstation o Windows 2000 Professional da cui l'utente può effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="09c43-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="09c43-107">Ogni nome NetBIOS è separato da una virgola.</span><span class="sxs-lookup"><span data-stu-id="09c43-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="09c43-108">Più nomi devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="09c43-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="09c43-109">Questo attributo utente non deve più essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="09c43-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="09c43-110">Per gestire gli account in grado di accedere alle workstation, è consigliabile utilizzare l'opzione "Consenti accesso locale" e "Nega accesso locale" o "Consenti accesso tramite Servizi Desktop remoto" e "Nega accesso tramite Servizi Desktop remoto".</span><span class="sxs-lookup"><span data-stu-id="09c43-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="09c43-111">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-111">Entry</span></span> | <span data-ttu-id="09c43-112">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c43-113">CN</span><span class="sxs-lookup"><span data-stu-id="09c43-113">CN</span></span>                | <span data-ttu-id="09c43-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="09c43-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="09c43-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="09c43-115">Ldap-Display-Name</span></span> | <span data-ttu-id="09c43-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="09c43-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="09c43-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="09c43-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="09c43-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="09c43-118">Update Privilege</span></span>  | <span data-ttu-id="09c43-119">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="09c43-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="09c43-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="09c43-120">Update Frequency</span></span>  | <span data-ttu-id="09c43-121">Quando il record dell'utente viene creato e ogni volta che è necessario modificare il privilegio di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09c43-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="09c43-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-122">Attribute-Id</span></span>      | <span data-ttu-id="09c43-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="09c43-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="09c43-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09c43-124">System-Id-Guid</span></span>    | <span data-ttu-id="09c43-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="09c43-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="09c43-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09c43-126">Syntax</span></span>            | [<span data-ttu-id="09c43-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="09c43-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="09c43-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="09c43-128">Implementations</span></span>

-   [<span data-ttu-id="09c43-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09c43-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09c43-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09c43-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09c43-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09c43-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09c43-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09c43-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09c43-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09c43-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09c43-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09c43-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09c43-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09c43-135">Windows 2000 Server</span></span>



| <span data-ttu-id="09c43-136">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-136">Entry</span></span> | <span data-ttu-id="09c43-137">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-140">System-Only</span></span>            | <span data-ttu-id="09c43-141">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-141">False</span></span>                             |
| <span data-ttu-id="09c43-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-142">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-143">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-143">True</span></span>                              |
| <span data-ttu-id="09c43-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-144">Is Indexed</span></span>             | <span data-ttu-id="09c43-145">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-145">False</span></span>                             |
| <span data-ttu-id="09c43-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-146">In Global Catalog</span></span>      | <span data-ttu-id="09c43-147">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-147">False</span></span>                             |
| <span data-ttu-id="09c43-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-150">Range-Lower</span></span>            | <span data-ttu-id="09c43-151">0</span><span class="sxs-lookup"><span data-stu-id="09c43-151">0</span></span>                                 |
| <span data-ttu-id="09c43-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-152">Range-Upper</span></span>            | <span data-ttu-id="09c43-153">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-153">1024</span></span>                              |
| <span data-ttu-id="09c43-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-154">Search-Flags</span></span>           | <span data-ttu-id="09c43-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-155">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-156">System-Flags</span></span>           | <span data-ttu-id="09c43-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-157">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-158">Classes used in</span></span>        | [<span data-ttu-id="09c43-159">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09c43-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09c43-160">Windows Server 2003</span></span>



| <span data-ttu-id="09c43-161">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-161">Entry</span></span> | <span data-ttu-id="09c43-162">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-165">System-Only</span></span>            | <span data-ttu-id="09c43-166">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-166">False</span></span>                             |
| <span data-ttu-id="09c43-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-167">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-168">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-168">True</span></span>                              |
| <span data-ttu-id="09c43-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-169">Is Indexed</span></span>             | <span data-ttu-id="09c43-170">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-170">False</span></span>                             |
| <span data-ttu-id="09c43-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-171">In Global Catalog</span></span>      | <span data-ttu-id="09c43-172">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-172">False</span></span>                             |
| <span data-ttu-id="09c43-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-175">Range-Lower</span></span>            | <span data-ttu-id="09c43-176">0</span><span class="sxs-lookup"><span data-stu-id="09c43-176">0</span></span>                                 |
| <span data-ttu-id="09c43-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-177">Range-Upper</span></span>            | <span data-ttu-id="09c43-178">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-178">1024</span></span>                              |
| <span data-ttu-id="09c43-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-179">Search-Flags</span></span>           | <span data-ttu-id="09c43-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-180">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-181">System-Flags</span></span>           | <span data-ttu-id="09c43-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-182">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-183">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-183">Classes used in</span></span>        | [<span data-ttu-id="09c43-184">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09c43-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09c43-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09c43-186">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-186">Entry</span></span> | <span data-ttu-id="09c43-187">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-190">System-Only</span></span>            | <span data-ttu-id="09c43-191">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-191">False</span></span>                             |
| <span data-ttu-id="09c43-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-192">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-193">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-193">True</span></span>                              |
| <span data-ttu-id="09c43-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-194">Is Indexed</span></span>             | <span data-ttu-id="09c43-195">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-195">False</span></span>                             |
| <span data-ttu-id="09c43-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-196">In Global Catalog</span></span>      | <span data-ttu-id="09c43-197">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-197">False</span></span>                             |
| <span data-ttu-id="09c43-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-200">Range-Lower</span></span>            | <span data-ttu-id="09c43-201">0</span><span class="sxs-lookup"><span data-stu-id="09c43-201">0</span></span>                                 |
| <span data-ttu-id="09c43-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-202">Range-Upper</span></span>            | <span data-ttu-id="09c43-203">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-203">1024</span></span>                              |
| <span data-ttu-id="09c43-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-204">Search-Flags</span></span>           | <span data-ttu-id="09c43-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-205">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-206">System-Flags</span></span>           | <span data-ttu-id="09c43-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-207">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-208">Classes used in</span></span>        | [<span data-ttu-id="09c43-209">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09c43-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09c43-210">Windows Server 2008</span></span>



| <span data-ttu-id="09c43-211">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-211">Entry</span></span> | <span data-ttu-id="09c43-212">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-215">System-Only</span></span>            | <span data-ttu-id="09c43-216">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-216">False</span></span>                             |
| <span data-ttu-id="09c43-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-217">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-218">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-218">True</span></span>                              |
| <span data-ttu-id="09c43-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-219">Is Indexed</span></span>             | <span data-ttu-id="09c43-220">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-220">False</span></span>                             |
| <span data-ttu-id="09c43-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-221">In Global Catalog</span></span>      | <span data-ttu-id="09c43-222">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-222">False</span></span>                             |
| <span data-ttu-id="09c43-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-225">Range-Lower</span></span>            | <span data-ttu-id="09c43-226">0</span><span class="sxs-lookup"><span data-stu-id="09c43-226">0</span></span>                                 |
| <span data-ttu-id="09c43-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-227">Range-Upper</span></span>            | <span data-ttu-id="09c43-228">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-228">1024</span></span>                              |
| <span data-ttu-id="09c43-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-229">Search-Flags</span></span>           | <span data-ttu-id="09c43-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-230">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-231">System-Flags</span></span>           | <span data-ttu-id="09c43-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-232">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-233">Classes used in</span></span>        | [<span data-ttu-id="09c43-234">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09c43-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09c43-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09c43-236">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-236">Entry</span></span> | <span data-ttu-id="09c43-237">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-238">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-240">System-Only</span></span>            | <span data-ttu-id="09c43-241">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-241">False</span></span>                             |
| <span data-ttu-id="09c43-242">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-242">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-243">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-243">True</span></span>                              |
| <span data-ttu-id="09c43-244">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-244">Is Indexed</span></span>             | <span data-ttu-id="09c43-245">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-245">False</span></span>                             |
| <span data-ttu-id="09c43-246">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-246">In Global Catalog</span></span>      | <span data-ttu-id="09c43-247">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-247">False</span></span>                             |
| <span data-ttu-id="09c43-248">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-249">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-250">Range-Lower</span></span>            | <span data-ttu-id="09c43-251">0</span><span class="sxs-lookup"><span data-stu-id="09c43-251">0</span></span>                                 |
| <span data-ttu-id="09c43-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-252">Range-Upper</span></span>            | <span data-ttu-id="09c43-253">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-253">1024</span></span>                              |
| <span data-ttu-id="09c43-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-254">Search-Flags</span></span>           | <span data-ttu-id="09c43-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-255">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-256">System-Flags</span></span>           | <span data-ttu-id="09c43-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-257">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-258">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-258">Classes used in</span></span>        | [<span data-ttu-id="09c43-259">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09c43-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09c43-260">Windows Server 2012</span></span>



| <span data-ttu-id="09c43-261">Voce</span><span class="sxs-lookup"><span data-stu-id="09c43-261">Entry</span></span> | <span data-ttu-id="09c43-262">Valore</span><span class="sxs-lookup"><span data-stu-id="09c43-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="09c43-263">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="09c43-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09c43-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="09c43-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="09c43-265">System-Only</span></span>            | <span data-ttu-id="09c43-266">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-266">False</span></span>                             |
| <span data-ttu-id="09c43-267">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="09c43-267">Is-Single-Valued</span></span>       | <span data-ttu-id="09c43-268">Vero</span><span class="sxs-lookup"><span data-stu-id="09c43-268">True</span></span>                              |
| <span data-ttu-id="09c43-269">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="09c43-269">Is Indexed</span></span>             | <span data-ttu-id="09c43-270">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-270">False</span></span>                             |
| <span data-ttu-id="09c43-271">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="09c43-271">In Global Catalog</span></span>      | <span data-ttu-id="09c43-272">Falso</span><span class="sxs-lookup"><span data-stu-id="09c43-272">False</span></span>                             |
| <span data-ttu-id="09c43-273">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="09c43-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="09c43-274">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="09c43-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="09c43-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09c43-275">Range-Lower</span></span>            | <span data-ttu-id="09c43-276">0</span><span class="sxs-lookup"><span data-stu-id="09c43-276">0</span></span>                                 |
| <span data-ttu-id="09c43-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09c43-277">Range-Upper</span></span>            | <span data-ttu-id="09c43-278">1024</span><span class="sxs-lookup"><span data-stu-id="09c43-278">1024</span></span>                              |
| <span data-ttu-id="09c43-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-279">Search-Flags</span></span>           | <span data-ttu-id="09c43-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-280">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09c43-281">System-Flags</span></span>           | <span data-ttu-id="09c43-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09c43-282">0x00000010</span></span>                        |
| <span data-ttu-id="09c43-283">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="09c43-283">Classes used in</span></span>        | [<span data-ttu-id="09c43-284">**Utente**</span><span class="sxs-lookup"><span data-stu-id="09c43-284">**User**</span></span>](c-user.md)<br/> |



 

 





