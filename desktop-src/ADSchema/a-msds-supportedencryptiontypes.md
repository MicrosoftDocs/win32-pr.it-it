---
title: attributi ms-DS-supported-Encryption-Types
description: Algoritmi di crittografia supportati da account utente, computer o attendibilità. Si noti che il KDC usa queste informazioni durante la generazione di un ticket di servizio per l'account.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo crittografia-supportato da MS-DS
- attributo msDS-SupportedEncryptionTypes-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303491"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="8e78f-105">attributi ms-DS-supported-Encryption-Types</span><span class="sxs-lookup"><span data-stu-id="8e78f-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="8e78f-106">Algoritmi di crittografia supportati da account utente, computer o attendibilità.</span><span class="sxs-lookup"><span data-stu-id="8e78f-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="8e78f-107">Il KDC usa queste informazioni durante la generazione di un ticket di servizio per l'account.</span><span class="sxs-lookup"><span data-stu-id="8e78f-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="8e78f-108">I servizi e i computer possono aggiornare automaticamente questo attributo sui rispettivi account in Active Directory e pertanto necessitano dell'accesso in scrittura a questo attributo.</span><span class="sxs-lookup"><span data-stu-id="8e78f-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="8e78f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="8e78f-109">Entry</span></span> | <span data-ttu-id="8e78f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="8e78f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8e78f-111">CN</span><span class="sxs-lookup"><span data-stu-id="8e78f-111">CN</span></span>                | <span data-ttu-id="8e78f-112">Tipi di crittografia supportati da MS-DS</span><span class="sxs-lookup"><span data-stu-id="8e78f-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="8e78f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8e78f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8e78f-114">msDS-SupportedEncryptionTypes</span><span class="sxs-lookup"><span data-stu-id="8e78f-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="8e78f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8e78f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="8e78f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8e78f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8e78f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8e78f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8e78f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e78f-118">Attribute-Id</span></span>      | <span data-ttu-id="8e78f-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="8e78f-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="8e78f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8e78f-120">System-Id-Guid</span></span>    | <span data-ttu-id="8e78f-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="8e78f-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="8e78f-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e78f-122">Syntax</span></span>            | [<span data-ttu-id="8e78f-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="8e78f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8e78f-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="8e78f-124">Implementations</span></span>

-   [<span data-ttu-id="8e78f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e78f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e78f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e78f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e78f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e78f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="8e78f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e78f-128">Windows Server 2008</span></span>



| <span data-ttu-id="8e78f-129">Voce</span><span class="sxs-lookup"><span data-stu-id="8e78f-129">Entry</span></span> | <span data-ttu-id="8e78f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8e78f-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e78f-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8e78f-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e78f-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e78f-133">System-Only</span></span>            | <span data-ttu-id="8e78f-134">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-134">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-135">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8e78f-135">Is-Single-Valued</span></span>       | <span data-ttu-id="8e78f-136">Vero</span><span class="sxs-lookup"><span data-stu-id="8e78f-136">True</span></span>                                                                                   |
| <span data-ttu-id="8e78f-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8e78f-137">Is Indexed</span></span>             | <span data-ttu-id="8e78f-138">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-138">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8e78f-139">In Global Catalog</span></span>      | <span data-ttu-id="8e78f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-140">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-141">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8e78f-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e78f-142">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8e78f-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="8e78f-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e78f-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e78f-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-145">Search-Flags</span></span>           | <span data-ttu-id="8e78f-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e78f-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="8e78f-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-147">System-Flags</span></span>           | <span data-ttu-id="8e78f-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e78f-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="8e78f-149">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8e78f-149">Classes used in</span></span>        | [<span data-ttu-id="8e78f-150">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="8e78f-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="8e78f-151">**Utente**</span><span class="sxs-lookup"><span data-stu-id="8e78f-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e78f-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e78f-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e78f-153">Voce</span><span class="sxs-lookup"><span data-stu-id="8e78f-153">Entry</span></span> | <span data-ttu-id="8e78f-154">Valore</span><span class="sxs-lookup"><span data-stu-id="8e78f-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e78f-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8e78f-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e78f-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e78f-157">System-Only</span></span>            | <span data-ttu-id="8e78f-158">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-158">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8e78f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8e78f-160">Vero</span><span class="sxs-lookup"><span data-stu-id="8e78f-160">True</span></span>                                                                                   |
| <span data-ttu-id="8e78f-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8e78f-161">Is Indexed</span></span>             | <span data-ttu-id="8e78f-162">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-162">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8e78f-163">In Global Catalog</span></span>      | <span data-ttu-id="8e78f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-164">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8e78f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e78f-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8e78f-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="8e78f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e78f-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e78f-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-169">Search-Flags</span></span>           | <span data-ttu-id="8e78f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e78f-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="8e78f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-171">System-Flags</span></span>           | <span data-ttu-id="8e78f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e78f-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="8e78f-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8e78f-173">Classes used in</span></span>        | [<span data-ttu-id="8e78f-174">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="8e78f-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="8e78f-175">**Utente**</span><span class="sxs-lookup"><span data-stu-id="8e78f-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e78f-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e78f-176">Windows Server 2012</span></span>



| <span data-ttu-id="8e78f-177">Voce</span><span class="sxs-lookup"><span data-stu-id="8e78f-177">Entry</span></span> | <span data-ttu-id="8e78f-178">Valore</span><span class="sxs-lookup"><span data-stu-id="8e78f-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e78f-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8e78f-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e78f-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="8e78f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e78f-181">System-Only</span></span>            | <span data-ttu-id="8e78f-182">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-182">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8e78f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8e78f-184">Vero</span><span class="sxs-lookup"><span data-stu-id="8e78f-184">True</span></span>                                                                                   |
| <span data-ttu-id="8e78f-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8e78f-185">Is Indexed</span></span>             | <span data-ttu-id="8e78f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-186">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8e78f-187">In Global Catalog</span></span>      | <span data-ttu-id="8e78f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8e78f-188">False</span></span>                                                                                  |
| <span data-ttu-id="8e78f-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8e78f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e78f-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8e78f-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="8e78f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e78f-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e78f-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="8e78f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-193">Search-Flags</span></span>           | <span data-ttu-id="8e78f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e78f-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="8e78f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e78f-195">System-Flags</span></span>           | <span data-ttu-id="8e78f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e78f-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="8e78f-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8e78f-197">Classes used in</span></span>        | [<span data-ttu-id="8e78f-198">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="8e78f-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="8e78f-199">**Utente**</span><span class="sxs-lookup"><span data-stu-id="8e78f-199">**User**</span></span>](c-user.md)<br/> |



 

 





