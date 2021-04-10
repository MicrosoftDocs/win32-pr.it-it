---
title: Controllo
description: Windows Filtering Platform (WFP) fornisce il controllo degli eventi correlati a firewall e IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103963625"
---
# <a name="auditing"></a><span data-ttu-id="66bcc-103">Controllo</span><span class="sxs-lookup"><span data-stu-id="66bcc-103">Auditing</span></span>

<span data-ttu-id="66bcc-104">Windows Filtering Platform (WFP) fornisce il controllo degli eventi correlati a firewall e IPsec.</span><span class="sxs-lookup"><span data-stu-id="66bcc-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="66bcc-105">Questi eventi vengono archiviati nel registro di sicurezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="66bcc-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="66bcc-106">Gli eventi controllati sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="66bcc-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bcc-107">Categoria di controllo</span><span class="sxs-lookup"><span data-stu-id="66bcc-107">Auditing category</span></span></th>
<th><span data-ttu-id="66bcc-108">Sottocategoria di controllo</span><span class="sxs-lookup"><span data-stu-id="66bcc-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="66bcc-109">Eventi controllati</span><span class="sxs-lookup"><span data-stu-id="66bcc-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bcc-110">Modifica dei criteri</span><span class="sxs-lookup"><span data-stu-id="66bcc-110">Policy Change</span></span><br/> <span data-ttu-id="66bcc-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-112">Modifica dei criteri della piattaforma di filtro</span><span class="sxs-lookup"><span data-stu-id="66bcc-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="66bcc-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="66bcc-114">I numeri rappresentano gli ID evento visualizzati da Visualizzatore eventi (eventvwr.exe).</span><span class="sxs-lookup"><span data-stu-id="66bcc-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="66bcc-115">Aggiunta e rimozione di oggetti WFP:</span><span class="sxs-lookup"><span data-stu-id="66bcc-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-116">5440 callout permanente aggiunto</span><span class="sxs-lookup"><span data-stu-id="66bcc-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="66bcc-117">5441 tempo di avvio o filtro permanente aggiunto</span><span class="sxs-lookup"><span data-stu-id="66bcc-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="66bcc-118">5442 provider persistente aggiunto</span><span class="sxs-lookup"><span data-stu-id="66bcc-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="66bcc-119">5443 contesto del provider persistente aggiunto</span><span class="sxs-lookup"><span data-stu-id="66bcc-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="66bcc-120">5444 sottolivello permanente aggiunto</span><span class="sxs-lookup"><span data-stu-id="66bcc-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="66bcc-121">5446 callout di run-time aggiunto o rimosso</span><span class="sxs-lookup"><span data-stu-id="66bcc-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="66bcc-122">5447 filtro di runtime aggiunto o rimosso</span><span class="sxs-lookup"><span data-stu-id="66bcc-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="66bcc-123">5448 provider di runtime aggiunto o rimosso</span><span class="sxs-lookup"><span data-stu-id="66bcc-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="66bcc-124">5449 contesto del provider di runtime aggiunto o rimosso</span><span class="sxs-lookup"><span data-stu-id="66bcc-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="66bcc-125">5450 sottolivello runtime aggiunto o rimosso</span><span class="sxs-lookup"><span data-stu-id="66bcc-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bcc-126">Accesso a oggetti</span><span class="sxs-lookup"><span data-stu-id="66bcc-126">Object Access</span></span><br/> <span data-ttu-id="66bcc-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-128">Eliminazione di pacchetti di piattaforma di filtro</span><span class="sxs-lookup"><span data-stu-id="66bcc-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="66bcc-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-130">Pacchetti eliminati da WFP:</span><span class="sxs-lookup"><span data-stu-id="66bcc-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-131">pacchetto 5152 rilasciato</span><span class="sxs-lookup"><span data-stu-id="66bcc-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="66bcc-132">pacchetto 5153 con veto</span><span class="sxs-lookup"><span data-stu-id="66bcc-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bcc-133">Accesso a oggetti</span><span class="sxs-lookup"><span data-stu-id="66bcc-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="66bcc-134">Connessione alla piattaforma di filtro</span><span class="sxs-lookup"><span data-stu-id="66bcc-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="66bcc-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-136">Connessioni consentite e bloccate:</span><span class="sxs-lookup"><span data-stu-id="66bcc-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-137">5154 ascolto consentito</span><span class="sxs-lookup"><span data-stu-id="66bcc-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="66bcc-138">5155 ascolto bloccato</span><span class="sxs-lookup"><span data-stu-id="66bcc-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="66bcc-139">connessione 5156 consentita</span><span class="sxs-lookup"><span data-stu-id="66bcc-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="66bcc-140">connessione 5157 bloccata</span><span class="sxs-lookup"><span data-stu-id="66bcc-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="66bcc-141">5158 associazione consentita</span><span class="sxs-lookup"><span data-stu-id="66bcc-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="66bcc-142">5159 binding bloccato</span><span class="sxs-lookup"><span data-stu-id="66bcc-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="66bcc-143">Le connessioni consentite non controllano sempre l'ID del filtro associato.</span><span class="sxs-lookup"><span data-stu-id="66bcc-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="66bcc-144">Il valore di FilterID per TCP sarà 0, a meno che non venga utilizzato un subset di queste condizioni di filtro: UserID, AppID, protocollo, porta remota.</span><span class="sxs-lookup"><span data-stu-id="66bcc-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bcc-145">Accesso a oggetti</span><span class="sxs-lookup"><span data-stu-id="66bcc-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="66bcc-146">Altri eventi di accesso agli oggetti</span><span class="sxs-lookup"><span data-stu-id="66bcc-146">Other Object Access Events</span></span><br/> <span data-ttu-id="66bcc-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="66bcc-148">Questa sottocategoria Abilita molti controlli.</span><span class="sxs-lookup"><span data-stu-id="66bcc-148">This subcategory enables many audits.</span></span> <span data-ttu-id="66bcc-149">I controlli specifici del WFP sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="66bcc-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="66bcc-150">Stato di prevenzione di attacchi Denial of Service:</span><span class="sxs-lookup"><span data-stu-id="66bcc-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-151">5148 modalità di prevenzione DoS PAM avviata</span><span class="sxs-lookup"><span data-stu-id="66bcc-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="66bcc-152">5149 modalità di prevenzione DoS PAM arrestata</span><span class="sxs-lookup"><span data-stu-id="66bcc-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bcc-153">Accesso/disconnessione</span><span class="sxs-lookup"><span data-stu-id="66bcc-153">Logon/Logoff</span></span><br/> <span data-ttu-id="66bcc-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-155">Modalità principale IPsec</span><span class="sxs-lookup"><span data-stu-id="66bcc-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="66bcc-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-157">Negoziazione in modalità principale IKE e AuthIP:</span><span class="sxs-lookup"><span data-stu-id="66bcc-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-158">4650, associazione di sicurezza 4651 stabilita</span><span class="sxs-lookup"><span data-stu-id="66bcc-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="66bcc-159">4652, negoziazione 4653 non riuscita</span><span class="sxs-lookup"><span data-stu-id="66bcc-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="66bcc-160">4655 associazione di sicurezza terminata</span><span class="sxs-lookup"><span data-stu-id="66bcc-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bcc-161">Accesso/disconnessione</span><span class="sxs-lookup"><span data-stu-id="66bcc-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="66bcc-162">Modalità rapida IPsec</span><span class="sxs-lookup"><span data-stu-id="66bcc-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="66bcc-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-164">Negoziazione in modalità rapida IKE e AuthIP:</span><span class="sxs-lookup"><span data-stu-id="66bcc-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-165">5451 associazione di sicurezza stabilita</span><span class="sxs-lookup"><span data-stu-id="66bcc-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="66bcc-166">5452 associazione di sicurezza terminata</span><span class="sxs-lookup"><span data-stu-id="66bcc-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="66bcc-167">negoziazione 4654 non riuscita</span><span class="sxs-lookup"><span data-stu-id="66bcc-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bcc-168">Accesso/disconnessione</span><span class="sxs-lookup"><span data-stu-id="66bcc-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="66bcc-169">Modalità estesa IPsec</span><span class="sxs-lookup"><span data-stu-id="66bcc-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="66bcc-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-171">Negoziazione in modalità estesa AuthIP:</span><span class="sxs-lookup"><span data-stu-id="66bcc-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-172">4978 pacchetto di negoziazione non valido</span><span class="sxs-lookup"><span data-stu-id="66bcc-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="66bcc-173">4979, 4980, 4981, 4982 associazione di sicurezza stabilita</span><span class="sxs-lookup"><span data-stu-id="66bcc-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="66bcc-174">4983, negoziazione 4984 non riuscita</span><span class="sxs-lookup"><span data-stu-id="66bcc-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bcc-175">Sistema</span><span class="sxs-lookup"><span data-stu-id="66bcc-175">System</span></span><br/> <span data-ttu-id="66bcc-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-177">Driver IPsec</span><span class="sxs-lookup"><span data-stu-id="66bcc-177">IPsec Driver</span></span><br/> <span data-ttu-id="66bcc-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="66bcc-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="66bcc-179">Pacchetti eliminati dal driver IPsec:</span><span class="sxs-lookup"><span data-stu-id="66bcc-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="66bcc-180">4963 pacchetto di testo non crittografato in ingresso eliminato</span><span class="sxs-lookup"><span data-stu-id="66bcc-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="66bcc-181">Per impostazione predefinita, il controllo per WFP è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="66bcc-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="66bcc-182">Il controllo può essere abilitato per ogni categoria tramite lo snap-in Editor oggetti Criteri di gruppo MMC, lo snap-in MMC Criteri di sicurezza locali o il comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="66bcc-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="66bcc-183">Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri, è possibile:</span><span class="sxs-lookup"><span data-stu-id="66bcc-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="66bcc-184">Usare il Editor oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="66bcc-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="66bcc-185">Eseguire **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="66bcc-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="66bcc-186">Espandere criteri del computer locale.</span><span class="sxs-lookup"><span data-stu-id="66bcc-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="66bcc-187">Espandere Configurazione computer.</span><span class="sxs-lookup"><span data-stu-id="66bcc-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="66bcc-188">Espandere impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="66bcc-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="66bcc-189">Espandere impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="66bcc-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="66bcc-190">Espandere Criteri locali.</span><span class="sxs-lookup"><span data-stu-id="66bcc-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="66bcc-191">Fare clic su criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="66bcc-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="66bcc-192">Fare doppio clic su Controlla modifiche dei criteri per avviare la finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="66bcc-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="66bcc-193">Controllare le caselle di controllo di esito positivo e negativo.</span><span class="sxs-lookup"><span data-stu-id="66bcc-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="66bcc-194">Usare i criteri di sicurezza locali</span><span class="sxs-lookup"><span data-stu-id="66bcc-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="66bcc-195">Eseguire **secpol. msc**.</span><span class="sxs-lookup"><span data-stu-id="66bcc-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="66bcc-196">Espandere Criteri locali.</span><span class="sxs-lookup"><span data-stu-id="66bcc-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="66bcc-197">Fare clic su criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="66bcc-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="66bcc-198">Fare doppio clic su Controlla modifiche dei criteri per avviare la finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="66bcc-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="66bcc-199">Controllare le caselle di controllo di esito positivo e negativo.</span><span class="sxs-lookup"><span data-stu-id="66bcc-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="66bcc-200">Usare il comando auditpol.exe</span><span class="sxs-lookup"><span data-stu-id="66bcc-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="66bcc-201">**auditpol/set/category: "modifica dei criteri"/Success: enable/failure: Enable**</span><span class="sxs-lookup"><span data-stu-id="66bcc-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="66bcc-202">Il controllo può essere abilitato in base alla sottocategoria solo tramite il comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="66bcc-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="66bcc-203">I nomi di categoria e sottocategoria di controllo sono localizzati.</span><span class="sxs-lookup"><span data-stu-id="66bcc-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="66bcc-204">Per evitare la localizzazione per gli script di controllo, è possibile usare i GUID corrispondenti al posto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="66bcc-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="66bcc-205">Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri della piattaforma di filtro è possibile usare uno dei comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66bcc-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="66bcc-206">**auditpol/set/SubCategory: "Filtering Platform policy change"/Success: enable/failure: Enable**</span><span class="sxs-lookup"><span data-stu-id="66bcc-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="66bcc-207">**auditpol/set/SubCategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/Success: enable/failure: Enable**</span><span class="sxs-lookup"><span data-stu-id="66bcc-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="66bcc-208">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66bcc-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="66bcc-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="66bcc-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="66bcc-210">[Registro eventi](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="66bcc-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="66bcc-211">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="66bcc-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

