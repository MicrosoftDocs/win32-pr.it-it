---
title: Servizio di autenticazione Internet & server dei criteri di rete
description: Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047511"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="e2662-103">Servizio di autenticazione Internet & server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="e2662-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="e2662-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).</span><span class="sxs-lookup"><span data-stu-id="e2662-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="e2662-105">Servizio di autenticazione Internet</span><span class="sxs-lookup"><span data-stu-id="e2662-105">Internet Authentication Service</span></span>

<span data-ttu-id="e2662-106">Il servizio di autenticazione Internet è l'implementazione Microsoft di un server e un proxy RADIUS.</span><span class="sxs-lookup"><span data-stu-id="e2662-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="e2662-107">Il servizio di autenticazione Internet supporta due set di API: API per le [estensioni server dei criteri di rete](ias-extensions.md) e [API oggetti dati server](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e2662-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="e2662-108">Per ulteriori informazioni su IAS, vedere [TechNet: servizio di autenticazione Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="e2662-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="e2662-109">Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="e2662-109">Network Policy Server</span></span>

<span data-ttu-id="e2662-110">Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS ed è disponibile nei server Windows a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e2662-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="e2662-111">Server dei criteri di rete supporta gli stessi due set di API IAS: API per le [estensioni del server dei criteri di rete](ias-extensions.md) e API per [oggetti dati del server](server-data-objects.md)</span><span class="sxs-lookup"><span data-stu-id="e2662-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="e2662-112">Server dei criteri di gruppo contiene inoltre un set di nuove funzionalità che espandono le funzionalità IAS.</span><span class="sxs-lookup"><span data-stu-id="e2662-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2662-113">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e2662-113">Feature</span></span></th>
<th><span data-ttu-id="e2662-114">Novità per NPS</span><span class="sxs-lookup"><span data-stu-id="e2662-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2662-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Protezione accesso alla rete (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="e2662-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="e2662-116">NPS è il server centrale di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="e2662-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="e2662-117">NPS supporta la creazione di criteri utilizzando le condizioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2662-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="e2662-118">Scadenza dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e2662-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="e2662-119">Versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e2662-119">Operating system version.</span></span></li>
<li><span data-ttu-id="e2662-120">Accedere all'indirizzo IP del client.</span><span class="sxs-lookup"><span data-stu-id="e2662-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="e2662-121">Criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="e2662-121">Health policies.</span></span></li>
<li><span data-ttu-id="e2662-122">Tipi EAP consentiti.</span><span class="sxs-lookup"><span data-stu-id="e2662-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="e2662-123">HCAP.</span><span class="sxs-lookup"><span data-stu-id="e2662-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="e2662-124">NPS supporta la creazione di criteri usando le seguenti impostazioni aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="e2662-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="e2662-125">Prova.</span><span class="sxs-lookup"><span data-stu-id="e2662-125">Probation.</span></span></li>
<li><span data-ttu-id="e2662-126">Accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="e2662-126">Limited access.</span></span></li>
<li><span data-ttu-id="e2662-127">Stato esteso per accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="e2662-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="e2662-128">Server dei criteri di rete, tramite NAP, interagisce con CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="e2662-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="e2662-129">IAS non supporta NAP.</span><span class="sxs-lookup"><span data-stu-id="e2662-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2662-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Criteri e supporto <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="e2662-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="e2662-131">NPS USA EAPHost per l'estendibilità del metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="e2662-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="e2662-132">Inoltre, gli amministratori possono configurare i criteri di accesso alla rete per EAP.</span><span class="sxs-lookup"><span data-stu-id="e2662-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="e2662-133">IAS non supporta l'integrazione EAPHost o le condizioni di filtro del tipo EAP per i criteri.</span><span class="sxs-lookup"><span data-stu-id="e2662-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2662-134">Supporto IPv6</span><span class="sxs-lookup"><span data-stu-id="e2662-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="e2662-135">NPS supporta la distribuzione in ambienti IPv6.</span><span class="sxs-lookup"><span data-stu-id="e2662-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="e2662-136">IAS non supporta indirizzi di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="e2662-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2662-137">Configurazione XML</span><span class="sxs-lookup"><span data-stu-id="e2662-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="e2662-138">La configurazione NPS può essere importata ed esportata in formato XML.</span><span class="sxs-lookup"><span data-stu-id="e2662-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="e2662-139">IAS utilizza un database Jet per l'archiviazione della configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="e2662-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2662-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Criteri comuni</a> Supporto</span><span class="sxs-lookup"><span data-stu-id="e2662-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="e2662-141">NPS è stato aggiornato per supportare la distribuzione in ambienti che devono soddisfare gli standard di sicurezza dei criteri comuni.</span><span class="sxs-lookup"><span data-stu-id="e2662-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2662-142"><a href="ias-extensions.md">API delle estensioni NPS</a></span><span class="sxs-lookup"><span data-stu-id="e2662-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="e2662-143">Le DLL di estensione NPS vengono eseguite in un processo separato dal servizio NPS.</span><span class="sxs-lookup"><span data-stu-id="e2662-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="e2662-144">In caso di arresto anomalo di una DLL di estensione, NPS continuerà a funzionare e le richieste future verranno rifiutate.</span><span class="sxs-lookup"><span data-stu-id="e2662-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="e2662-145">Le DLL di estensione IAS vengono eseguite nello stesso processo del servizio IAS e possono influire negativamente sul servizio.</span><span class="sxs-lookup"><span data-stu-id="e2662-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2662-146">Interfaccia utente di gestione</span><span class="sxs-lookup"><span data-stu-id="e2662-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="e2662-147">La console di gestione NPS (NPS. msc) ha un nuovo aspetto, una migliore usabilità e tutte le nuove funzionalità aggiunte al server dei criteri di server.</span><span class="sxs-lookup"><span data-stu-id="e2662-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="e2662-148">IAS utilizza la console di gestione IAS. msc.</span><span class="sxs-lookup"><span data-stu-id="e2662-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2662-149">Strumento di gestione dei ruoli e integrazione Server Manager</span><span class="sxs-lookup"><span data-stu-id="e2662-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="e2662-150">NPS è integrato con il Server Manager e lo strumento di gestione dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="e2662-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="e2662-151">Questa integrazione semplifica la configurazione e la gestione di NPS e di scenari correlati.</span><span class="sxs-lookup"><span data-stu-id="e2662-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="e2662-152">Server Manager non è disponibile nei computer che eseguono IAS.</span><span class="sxs-lookup"><span data-stu-id="e2662-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2662-153">Aggiornamento dello script della riga di comando con <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="e2662-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="e2662-154">NPS supporta l' &quot; interfaccia della &quot; riga di comando netsh NPS.</span><span class="sxs-lookup"><span data-stu-id="e2662-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="e2662-155">&quot;Netsh NPS &quot; contiene nuovi comandi che consentono di configurare completamente NPS, incluse le funzionalità di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="e2662-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="e2662-156">IAS supporta l' &quot; interfaccia della &quot; riga di comando netsh aaaa.</span><span class="sxs-lookup"><span data-stu-id="e2662-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2662-157">Isolamento dei criteri</span><span class="sxs-lookup"><span data-stu-id="e2662-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="e2662-158">NPS consente l'implementazione dell'isolamento dei criteri impostando l'origine dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="e2662-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="e2662-159">È possibile configurare i criteri che sono applicabili solo a un tipo NAS predeterminato.</span><span class="sxs-lookup"><span data-stu-id="e2662-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="e2662-160">IAS non supporta l'isolamento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e2662-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e2662-161">Per ulteriori informazioni su NPS, vedere [TechNet: Server dei criteri di rete](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="e2662-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2662-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2662-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2662-163">Autenticazione, autorizzazione e accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="e2662-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="e2662-164">Registrazione con server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="e2662-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="e2662-165">Utilizzo di un server di stato</span><span class="sxs-lookup"><span data-stu-id="e2662-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

