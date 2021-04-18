---
title: IPv6-Aware e funzioni helper WPAD legacy
description: Differenze tra IPv6-Aware funzioni helper WPAD e funzioni helper WPAD legacy
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316011"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="644f8-103">IPv6-Aware e funzioni helper WPAD legacy</span><span class="sxs-lookup"><span data-stu-id="644f8-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="644f8-104">Le tabelle seguenti illustrano le differenze tra le nuove funzioni helper WPAD e le funzioni helper WPAD legacy.</span><span class="sxs-lookup"><span data-stu-id="644f8-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="644f8-105">Le nuove funzioni sono contrassegnate da un asterisco.</span><span class="sxs-lookup"><span data-stu-id="644f8-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="644f8-106">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-106">Functions</span></span></th>
<th><span data-ttu-id="644f8-107">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-107">Input</span></span></th>
<th><span data-ttu-id="644f8-108">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-108">Output</span></span></th>
<th><span data-ttu-id="644f8-109">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="644f8-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="644f8-110">dnsResolve</span></span></td>
<td><span data-ttu-id="644f8-111">Host</span><span class="sxs-lookup"><span data-stu-id="644f8-111">Host</span></span></td>
<td><span data-ttu-id="644f8-112">IPv4 address (Indirizzo IPv4)</span><span class="sxs-lookup"><span data-stu-id="644f8-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="644f8-113">La funzione ex restituirà un elenco di IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="644f8-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="644f8-114">Necessario perché gli indirizzi IPv6 o IPv4 possono avere più indirizzi unicast per una singola interfaccia. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="644f8-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="644f8-115">dnsResolveEx\*</span><span class="sxs-lookup"><span data-stu-id="644f8-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="644f8-116">Host</span><span class="sxs-lookup"><span data-stu-id="644f8-116">Host</span></span></td>
<td><span data-ttu-id="644f8-117">Elenco di indirizzi IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="644f8-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-118">Functions</span></span></th>
<th><span data-ttu-id="644f8-119">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-119">Input</span></span></th>
<th><span data-ttu-id="644f8-120">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-120">Output</span></span></th>
<th><span data-ttu-id="644f8-121">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="644f8-122">con risoluzione</span><span class="sxs-lookup"><span data-stu-id="644f8-122">isResolveable</span></span></td>
<td><span data-ttu-id="644f8-123">Host IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-123">IPv4 host</span></span></td>
<td><span data-ttu-id="644f8-124">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="644f8-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="644f8-125">La funzione ex restituirà TRUE se un host può essere risolto in un indirizzo IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="644f8-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="644f8-126">La funzione legacy restituisce TRUE solo se l'host viene risolto in un indirizzo IPv4. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="644f8-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="644f8-127">isResolveableEx\*</span><span class="sxs-lookup"><span data-stu-id="644f8-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="644f8-128">Host IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="644f8-129">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="644f8-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="644f8-130">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-130">Functions</span></span></th>
<th><span data-ttu-id="644f8-131">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-131">Input</span></span></th>
<th><span data-ttu-id="644f8-132">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-132">Output</span></span></th>
<th><span data-ttu-id="644f8-133">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="644f8-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="644f8-134">myIPAddress</span></span></td>
<td><span data-ttu-id="644f8-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="644f8-135">none</span></span></td>
<td><span data-ttu-id="644f8-136">IPv4 address (Indirizzo IPv4)</span><span class="sxs-lookup"><span data-stu-id="644f8-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="644f8-137">La funzione ex restituirà un elenco di IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="644f8-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="644f8-138">Necessario perché gli indirizzi IPv6 o IPv4 possono avere più indirizzi unicast per una singola interfaccia $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="644f8-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="644f8-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="644f8-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="644f8-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="644f8-140">none</span></span></td>
<td><span data-ttu-id="644f8-141">Elenco di indirizzi IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="644f8-142">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-142">Functions</span></span></th>
<th><span data-ttu-id="644f8-143">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-143">Input</span></span></th>
<th><span data-ttu-id="644f8-144">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-144">Output</span></span></th>
<th><span data-ttu-id="644f8-145">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="644f8-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="644f8-146">isInNet</span></span></td>
<td><span data-ttu-id="644f8-147">Host, modello di indirizzo IP separato da punti, maschera di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="644f8-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="644f8-148">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="644f8-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="644f8-149">Fornire una modalità indipendente dalla versione IP per individuare se un indirizzo IP si trova in una determinata subnet.</span><span class="sxs-lookup"><span data-stu-id="644f8-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="644f8-150">Inoltre, la notazione della maschera in IPv4 è deprecata. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="644f8-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="644f8-151">isInNetEx\*</span><span class="sxs-lookup"><span data-stu-id="644f8-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="644f8-152">Prefisso IP indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="644f8-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="644f8-153">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="644f8-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="644f8-154">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-154">Functions</span></span>           | <span data-ttu-id="644f8-155">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-155">Input</span></span>                       | <span data-ttu-id="644f8-156">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-156">Output</span></span>                             | <span data-ttu-id="644f8-157">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="644f8-158">sortIPAddressList\*</span><span class="sxs-lookup"><span data-stu-id="644f8-158">sortIPAddressList\*</span></span> | <span data-ttu-id="644f8-159">Elenco di indirizzi IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="644f8-160">Elenco ordinato di indirizzi IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="644f8-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="644f8-161">Non esiste alcuna funzione legacy di controparte poiché le funzioni legacy restituiscono solo un singolo indirizzo IPv4, pertanto non è necessario eseguire l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="644f8-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="644f8-162">Funzioni</span><span class="sxs-lookup"><span data-stu-id="644f8-162">Functions</span></span>          | <span data-ttu-id="644f8-163">Input</span><span class="sxs-lookup"><span data-stu-id="644f8-163">Input</span></span> | <span data-ttu-id="644f8-164">Output</span><span class="sxs-lookup"><span data-stu-id="644f8-164">Output</span></span>                     | <span data-ttu-id="644f8-165">Motivo della modifica</span><span class="sxs-lookup"><span data-stu-id="644f8-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="644f8-166">getClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="644f8-166">getClientVersion\*</span></span> | <span data-ttu-id="644f8-167">Nessuno</span><span class="sxs-lookup"><span data-stu-id="644f8-167">none</span></span>  | <span data-ttu-id="644f8-168">Numero di versione del motore WPAD</span><span class="sxs-lookup"><span data-stu-id="644f8-168">WPAD engine version number</span></span> | <span data-ttu-id="644f8-169">Attualmente questa funzione restituisce la versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="644f8-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="644f8-170">Questa funzione è stata aggiunta per consentire agli amministratori IT di aggiornare WPAD in modo che funzionino con versioni diverse del motore WPAD senza causare interruzioni della distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="644f8-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="644f8-171">Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="644f8-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



