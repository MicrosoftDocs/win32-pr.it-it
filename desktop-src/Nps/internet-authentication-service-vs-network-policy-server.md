---
title: Servizio di autenticazione Internet & Server dei criteri di rete
description: Informazioni sul servizio di autenticazione Internet e sul server dei criteri di rete. Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989426"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="9123d-104">Servizio di autenticazione Internet & Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9123d-104">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="9123d-105">Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="9123d-106">Servizio di autenticazione Internet</span><span class="sxs-lookup"><span data-stu-id="9123d-106">Internet Authentication Service</span></span>

<span data-ttu-id="9123d-107">Il servizio di autenticazione Internet è l'implementazione Microsoft di un server RADIUS e di un proxy.</span><span class="sxs-lookup"><span data-stu-id="9123d-107">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="9123d-108">Il servizio di autenticazione Internet supporta due set di API: [l'API delle estensioni del server dei](ias-extensions.md) criteri di rete e l'API oggetti dati del [server](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9123d-108">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="9123d-109">Per altre informazioni su IAS, vedere [TechNet: Servizio](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) di autenticazione Internet.</span><span class="sxs-lookup"><span data-stu-id="9123d-109">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="9123d-110">Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9123d-110">Network Policy Server</span></span>

<span data-ttu-id="9123d-111">Server dei criteri di rete è l'implementazione Microsoft di un server RADIUS e di un proxy ed è disponibile nei server Windows a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9123d-111">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="9123d-112">Server dei criteri di rete supporta gli stessi due set di API di IAS: [l'API delle](ias-extensions.md) estensioni del server dei criteri di rete e l'API oggetti dati del [server](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9123d-112">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="9123d-113">Server dei criteri di rete contiene anche un set di nuove funzionalità che espandono le funzionalità IAS.</span><span class="sxs-lookup"><span data-stu-id="9123d-113">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9123d-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="9123d-114">Feature</span></span></th>
<th><span data-ttu-id="9123d-115">Novità di Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9123d-115">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9123d-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Protezione accesso alla rete (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="9123d-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="9123d-117">Server dei criteri di rete è il server centrale di Protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-117">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="9123d-118">Server dei criteri di rete supporta la creazione di criteri utilizzando le condizioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="9123d-118">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="9123d-119">Scadenza dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9123d-119">Policy expiration.</span></span></li>
<li><span data-ttu-id="9123d-120">Versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9123d-120">Operating system version.</span></span></li>
<li><span data-ttu-id="9123d-121">Accedere all'indirizzo IP del client.</span><span class="sxs-lookup"><span data-stu-id="9123d-121">Access client IP address.</span></span></li>
<li><span data-ttu-id="9123d-122">Criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="9123d-122">Health policies.</span></span></li>
<li><span data-ttu-id="9123d-123">Tipi EAP consentiti.</span><span class="sxs-lookup"><span data-stu-id="9123d-123">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="9123d-124">Hcap.</span><span class="sxs-lookup"><span data-stu-id="9123d-124">HCAP.</span></span></li>
</ul>
<span data-ttu-id="9123d-125">Server dei criteri di rete supporta la creazione di criteri usando le impostazioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="9123d-125">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="9123d-126">Prova.</span><span class="sxs-lookup"><span data-stu-id="9123d-126">Probation.</span></span></li>
<li><span data-ttu-id="9123d-127">Accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="9123d-127">Limited access.</span></span></li>
<li><span data-ttu-id="9123d-128">Stato esteso per accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="9123d-128">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="9123d-129">Server dei criteri di rete, tramite Protezione accesso alla rete, interagisce con CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="9123d-129">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="9123d-130">IAS non supporta Protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-130">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9123d-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Supporto di <a href="/windows/win32/eaphost/portal">criteri ed EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="9123d-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="9123d-132">Server dei criteri di rete usa EAPHost per l'estendibilità dei metodi EAP.</span><span class="sxs-lookup"><span data-stu-id="9123d-132">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="9123d-133">Inoltre, gli amministratori possono configurare i criteri di accesso alla rete per EAP.</span><span class="sxs-lookup"><span data-stu-id="9123d-133">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="9123d-134">IAS non supporta l'integrazione EAPHost o le condizioni di filtro del tipo EAP per i criteri.</span><span class="sxs-lookup"><span data-stu-id="9123d-134">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9123d-135">Supporto IPv6</span><span class="sxs-lookup"><span data-stu-id="9123d-135">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="9123d-136">Server dei criteri di rete supporta la distribuzione in ambienti IPv6.</span><span class="sxs-lookup"><span data-stu-id="9123d-136">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="9123d-137">IAS non supporta gli indirizzi di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="9123d-137">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9123d-138">Configurazione XML</span><span class="sxs-lookup"><span data-stu-id="9123d-138">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="9123d-139">La configurazione di Server dei criteri di rete può essere importata ed esportata in formato XML.</span><span class="sxs-lookup"><span data-stu-id="9123d-139">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="9123d-140">IAS usa un database Jet per archiviare la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="9123d-140">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9123d-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Criteri comuni</a> Supporto</span><span class="sxs-lookup"><span data-stu-id="9123d-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="9123d-142">Server dei criteri di rete è stato aggiornato per supportare la distribuzione in ambienti che devono soddisfare gli standard di sicurezza dei criteri comuni.</span><span class="sxs-lookup"><span data-stu-id="9123d-142">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9123d-143"><a href="ias-extensions.md">NPS Extensions API</a></span><span class="sxs-lookup"><span data-stu-id="9123d-143"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="9123d-144">Le DLL dell'estensione NPS vengono eseguite in un processo separato dal servizio Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-144">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="9123d-145">In caso di arresto anomalo della DLL di estensione, Server dei criteri di rete continuerà a essere in esecuzione e le richieste future verranno rifiutate.</span><span class="sxs-lookup"><span data-stu-id="9123d-145">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="9123d-146">Le DLL di estensione IAS vengono eseguite nello stesso processo del servizio IAS e possono influire negativamente sul servizio.</span><span class="sxs-lookup"><span data-stu-id="9123d-146">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9123d-147">Gestione Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9123d-147">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="9123d-148">La console di gestione server dei criteri di rete (nps.msc) ha un nuovo aspetto, usabilità migliorata e copre tutte le nuove funzionalità aggiunte a Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-148">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="9123d-149">IAS usa la console di gestione ias.msc.</span><span class="sxs-lookup"><span data-stu-id="9123d-149">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9123d-150">Strumento di gestione dei ruoli e integrazione Server Manager ruoli</span><span class="sxs-lookup"><span data-stu-id="9123d-150">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="9123d-151">Server dei criteri di rete è integrato con Server Manager e lo strumento di gestione dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="9123d-151">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="9123d-152">Questa integrazione facilita la configurazione e la gestione di Server dei criteri di rete e degli scenari correlati.</span><span class="sxs-lookup"><span data-stu-id="9123d-152">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="9123d-153">Server Manager non è disponibile nei computer che eseguono IAS.</span><span class="sxs-lookup"><span data-stu-id="9123d-153">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9123d-154">Aggiornamento dello scripting della riga di comando <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">con Netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="9123d-154">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="9123d-155">Server dei criteri di rete supporta &quot; l'interfaccia della riga di comando netsh nps. &quot;</span><span class="sxs-lookup"><span data-stu-id="9123d-155">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="9123d-156">&quot;Netsh nps contiene nuovi comandi che consentono di configurare completamente Server dei criteri di &quot; rete, incluse le funzionalità di Protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-156">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="9123d-157">IAS supporta l'interfaccia della riga di comando &quot; Netsh aaaa. &quot;</span><span class="sxs-lookup"><span data-stu-id="9123d-157">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9123d-158">Isolamento dei criteri</span><span class="sxs-lookup"><span data-stu-id="9123d-158">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="9123d-159">Server dei criteri di rete consente l'implementazione dell'isolamento dei criteri impostando l'origine dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-159">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="9123d-160">È possibile configurare criteri applicabili solo a un tipo NAS predeterminato.</span><span class="sxs-lookup"><span data-stu-id="9123d-160">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="9123d-161">IAS non supporta l'isolamento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9123d-161">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9123d-162">Per altre informazioni su Server dei criteri di rete, vedere [TechNet: Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="9123d-162">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9123d-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9123d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9123d-164">Autenticazione, autorizzazione e accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="9123d-164">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="9123d-165">Registrazione con server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9123d-165">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="9123d-166">Utilizzo di un server di stato</span><span class="sxs-lookup"><span data-stu-id="9123d-166">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

