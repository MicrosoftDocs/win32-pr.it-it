---
title: attributo ms-DS-REPL-Authentication-Mode
description: L'attributo ms-DS-REPL-Authentication-Mode viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-REPL-Authentication-Mode
- attributo msDS-ReplAuthenticationMode-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480360"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="0981e-105">attributo ms-DS-REPL-Authentication-Mode</span><span class="sxs-lookup"><span data-stu-id="0981e-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="0981e-106">L'attributo **ms-DS-REPL-Authentication-Mode** viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica.</span><span class="sxs-lookup"><span data-stu-id="0981e-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="0981e-107">Questo attributo si applica alla partizione di configurazione di un'istanza ADAM.</span><span class="sxs-lookup"><span data-stu-id="0981e-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="0981e-108">Di seguito sono riportati i valori possibili per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="0981e-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="0981e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0981e-109">Value</span></span>        | <span data-ttu-id="0981e-110">Metodo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="0981e-110">Authentication method</span></span>                          | <span data-ttu-id="0981e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0981e-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0981e-112">0</span><span class="sxs-lookup"><span data-stu-id="0981e-112">0</span></span><br/> | <span data-ttu-id="0981e-113">Negoziata pass-through</span><span class="sxs-lookup"><span data-stu-id="0981e-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="0981e-114">Tutte le istanze di ADAM nel set di configurazione utilizzano un nome account e una password identici a quelli dell'account del servizio ADAM.</span><span class="sxs-lookup"><span data-stu-id="0981e-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="0981e-115">1</span><span class="sxs-lookup"><span data-stu-id="0981e-115">1</span></span><br/> | <span data-ttu-id="0981e-116">Negoziata</span><span class="sxs-lookup"><span data-stu-id="0981e-116">Negotiated</span></span><br/>                          | <span data-ttu-id="0981e-117">Viene in primo luogo eseguita l'autenticazione Kerberos mediante SPN.</span><span class="sxs-lookup"><span data-stu-id="0981e-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="0981e-118">Se l'autenticazione Kerberos non riesce, viene eseguita l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="0981e-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="0981e-119">Se NTLM ha esito negativo, le istanze di ADAM non vengono replicate.</span><span class="sxs-lookup"><span data-stu-id="0981e-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="0981e-120">2</span><span class="sxs-lookup"><span data-stu-id="0981e-120">2</span></span><br/> | <span data-ttu-id="0981e-121">Autenticazione manuale con Kerberos</span><span class="sxs-lookup"><span data-stu-id="0981e-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="0981e-122">È necessaria l'autenticazione Kerberos, tramite i nomi principali di servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="0981e-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="0981e-123">Se l'autenticazione Kerberos ha esito negativo, le istanze di ADAM non vengono replicate.</span><span class="sxs-lookup"><span data-stu-id="0981e-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="0981e-124">La tabella seguente contiene gli identificatori programmatici per i valori di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="0981e-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="0981e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0981e-125">Value</span></span>        | <span data-ttu-id="0981e-126">Identificatore (da NTDSAPI. h)</span><span class="sxs-lookup"><span data-stu-id="0981e-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0981e-127">0</span><span class="sxs-lookup"><span data-stu-id="0981e-127">0</span></span><br/> | <span data-ttu-id="0981e-128">**il \_ \_ pass- \_ \_ through Negotiate \_ \_ in modalità di autenticazione Adam repl**</span><span class="sxs-lookup"><span data-stu-id="0981e-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="0981e-129">1</span><span class="sxs-lookup"><span data-stu-id="0981e-129">1</span></span><br/> | <span data-ttu-id="0981e-130">**\_ \_ negoziazione modalità di autenticazione Adam REPL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0981e-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="0981e-131">2</span><span class="sxs-lookup"><span data-stu-id="0981e-131">2</span></span><br/> | <span data-ttu-id="0981e-132">**ADAM \_ REPL \_ modalità di autenticazione \_ \_ reciproca-autenticazione \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="0981e-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="0981e-133">Voce</span><span class="sxs-lookup"><span data-stu-id="0981e-133">Entry</span></span> | <span data-ttu-id="0981e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0981e-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0981e-135">CN</span><span class="sxs-lookup"><span data-stu-id="0981e-135">CN</span></span>                | <span data-ttu-id="0981e-136">ms-DS-REPL-Authentication-Mode</span><span class="sxs-lookup"><span data-stu-id="0981e-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="0981e-137">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0981e-137">Ldap-Display-Name</span></span> | <span data-ttu-id="0981e-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="0981e-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="0981e-139">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0981e-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="0981e-140">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0981e-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0981e-141">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0981e-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0981e-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0981e-142">Attribute-Id</span></span>      | <span data-ttu-id="0981e-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="0981e-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="0981e-144">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0981e-144">System-Id-Guid</span></span>    | <span data-ttu-id="0981e-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="0981e-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="0981e-146">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0981e-146">Syntax</span></span>            | [<span data-ttu-id="0981e-147">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="0981e-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0981e-148">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0981e-148">Implementations</span></span>

-   [<span data-ttu-id="0981e-149">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0981e-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="0981e-150">ADAM</span><span class="sxs-lookup"><span data-stu-id="0981e-150">ADAM</span></span>



| <span data-ttu-id="0981e-151">Voce</span><span class="sxs-lookup"><span data-stu-id="0981e-151">Entry</span></span> | <span data-ttu-id="0981e-152">Valore</span><span class="sxs-lookup"><span data-stu-id="0981e-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="0981e-153">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0981e-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="0981e-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0981e-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="0981e-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="0981e-155">System-Only</span></span>            | <span data-ttu-id="0981e-156">Falso</span><span class="sxs-lookup"><span data-stu-id="0981e-156">False</span></span>                                               |
| <span data-ttu-id="0981e-157">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0981e-157">Is-Single-Valued</span></span>       | <span data-ttu-id="0981e-158">Vero</span><span class="sxs-lookup"><span data-stu-id="0981e-158">True</span></span>                                                |
| <span data-ttu-id="0981e-159">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0981e-159">Is Indexed</span></span>             | <span data-ttu-id="0981e-160">Falso</span><span class="sxs-lookup"><span data-stu-id="0981e-160">False</span></span>                                               |
| <span data-ttu-id="0981e-161">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0981e-161">In Global Catalog</span></span>      | <span data-ttu-id="0981e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="0981e-162">False</span></span>                                               |
| <span data-ttu-id="0981e-163">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0981e-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="0981e-164">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0981e-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="0981e-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0981e-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="0981e-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0981e-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="0981e-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0981e-167">Search-Flags</span></span>           | <span data-ttu-id="0981e-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0981e-168">0x00000000</span></span>                                          |
| <span data-ttu-id="0981e-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0981e-169">System-Flags</span></span>           | <span data-ttu-id="0981e-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0981e-170">0x00000010</span></span>                                          |
| <span data-ttu-id="0981e-171">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0981e-171">Classes used in</span></span>        | [<span data-ttu-id="0981e-172">**Configurazione**</span><span class="sxs-lookup"><span data-stu-id="0981e-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





