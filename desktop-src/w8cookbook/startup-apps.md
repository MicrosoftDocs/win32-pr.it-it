---
title: App di avvio
description: App di avvio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- app di avvio
- attività in background
- Esegui chiave
- RunOnce
- cartella di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734631"
---
# <a name="startup-apps"></a><span data-ttu-id="1a8dc-108">App di avvio</span><span class="sxs-lookup"><span data-stu-id="1a8dc-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="1a8dc-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="1a8dc-109">Platform</span></span>

<span data-ttu-id="1a8dc-110">**Client**   di   Windows 8</span><span class="sxs-lookup"><span data-stu-id="1a8dc-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="1a8dc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a8dc-111">Description</span></span>

<span data-ttu-id="1a8dc-112">Una delle principali scommesse con Windows è la possibilità di creare diversi fattori di forma, da desktop e portatili tradizionali a tablet a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="1a8dc-113">Per garantire che i nostri clienti reciproci abbiano un'esperienza eccezionale su qualsiasi fattore di forma che scelgono con Windows, due metriche di successo chiave che devono essere risolte sono una maggiore durata della batteria e una velocità di risposta del PC eccellente.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="1a8dc-114">Per ottenere questi risultati, sono stati apportati miglioramenti in più aree di Windows, tra cui il ciclo di vita del processo, gli Stati di sospensione e le app di avvio (app con avvio automatico dopo l'avvio del computer).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="1a8dc-115">In questo argomento vengono illustrati alcuni degli effetti sulle app di avvio in un dispositivo Windows e vengono fornite indicazioni per sviluppatori (ISV/IHV) e OEM per ripensare ai modelli di utilizzo delle app di avvio per migliorare la durata e la velocità di risposta della batteria per i clienti reciproci.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="1a8dc-116">Vengono inoltre descritte le modifiche apportate in Windows che consentono agli utenti di controllare la determinazione delle app di avvio effettivamente da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="1a8dc-117">Le app di Windows Store sono progettate per essere conformi ai nuovi standard di consumo e velocità di risposta della batteria e Windows gestisce il proprio ciclo di vita sospendendo e/o terminando tali app.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="1a8dc-118">Tuttavia, le applicazioni desktop progettate per le versioni precedenti di Windows non sono necessariamente state progettate per preservare la durata della batteria o essere sensibili alle attività degli utenti e possono influenzare la velocità di risposta del sistema, ad esempio quando un'app invia un normale heartbeat di 1 secondo per verificare la disponibilità di aggiornamenti o pre-alloca la memoria in anticipo, se necessario in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="1a8dc-119">Questo può creare un'esperienza insufficiente per l'utente che acquista un Tablet PC Windows con una lunga permanenza della batteria e settimane di standby, ma rileva che la durata della batteria della tavoletta non raggiunge questi obiettivi.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="1a8dc-120">Inoltre, poiché le app di avvio vengono eseguite in background, il numero di app in esecuzione nel sistema può essere significativamente superiore rispetto a quello che l'utente è a conoscenza e influisce sulla velocità di risposta del sistema.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="1a8dc-121">Le app di avvio sono classificate in modo da includere quelle che sfruttano questi meccanismi per iniziare:</span><span class="sxs-lookup"><span data-stu-id="1a8dc-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="1a8dc-122">Eseguire le chiavi del registro di sistema (i nodi HKLM, HKCU, WOW64 sono inclusi)</span><span class="sxs-lookup"><span data-stu-id="1a8dc-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="1a8dc-123">Chiavi del registro di sistema RunOnce</span><span class="sxs-lookup"><span data-stu-id="1a8dc-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="1a8dc-124">Cartelle di avvio nel menu Start per ogni utente e località pubbliche</span><span class="sxs-lookup"><span data-stu-id="1a8dc-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="1a8dc-125">Nuove funzionalità sono state aggiunte a Windows per garantire che gli utenti finali siano sempre in grado di controllare le app eseguite nei sistemi.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="1a8dc-126">La scheda Startup in Gestione attività Mostra un elenco di app di avvio, insieme ai controlli che consentono agli utenti di disabilitare le app di avvio.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="1a8dc-127">Per consentire agli utenti di determinare gli elementi da disabilitare, gestione attività Visualizza una misura di ogni effetto dell'app di avvio.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="1a8dc-128">L'effetto viene valutato in base all'utilizzo della CPU e del disco dell'app all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="1a8dc-129">I valori di effetto vengono determinati applicando questi criteri:</span><span class="sxs-lookup"><span data-stu-id="1a8dc-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="1a8dc-130">**Effetto elevato**   App che usano più di un secondo di tempo di CPU o più di 3 MB di I/O su disco all'avvio</span><span class="sxs-lookup"><span data-stu-id="1a8dc-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="1a8dc-131">**Effetto medio**   App che usano 300 ms-1000 ms di tempo di CPU o 300 KB-3 MB di I/O su disco</span><span class="sxs-lookup"><span data-stu-id="1a8dc-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="1a8dc-132">**Basso effetto**   App che usano meno di 300 ms di tempo di CPU e inferiori a 300 KB di I/O su disco</span><span class="sxs-lookup"><span data-stu-id="1a8dc-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="1a8dc-133">Microsoft offre strumenti che consentono agli sviluppatori di app di valutare, analizzare e intraprendere le misure per ridurre l'effetto di avvio e migliorare l'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="1a8dc-134">Il kit Assessment and Deployment fornisce la possibilità di eseguire una valutazione delle prestazioni di avvio e di misurare l'impatto delle app eseguite all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="1a8dc-135">I risultati della valutazione contengono informazioni dettagliate su analisi e monitoraggio e aggiornamento, ove applicabile, per i componenti che hanno un impatto superiore all'avvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="1a8dc-136">Con Windows Performance Analyzer, gli sviluppatori di app possono eseguire analisi approfondite per trovare la causa radice dell'effetto sulle prestazioni e migliorare le prestazioni di avvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="1a8dc-137">Installare Windows ADK da [qui](/previous-versions/windows/hh825494(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="1a8dc-138">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="1a8dc-138">Guidance</span></span>

<span data-ttu-id="1a8dc-139">Le app di avvio si estendono su più categorie, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="1a8dc-140">Un set di raccomandazioni per gli sviluppatori viene mappato alle categorie di app di avvio per allinearsi alle modifiche funzionali di Windows descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="1a8dc-141">Categorie di app di avvio</span><span class="sxs-lookup"><span data-stu-id="1a8dc-141">Startup Apps Categories</span></span>

<span data-ttu-id="1a8dc-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a8dc-142">Description</span></span>

<span data-ttu-id="1a8dc-143">Recommendation</span><span class="sxs-lookup"><span data-stu-id="1a8dc-143">Recommendation</span></span>

<span data-ttu-id="1a8dc-144">**Quelli**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-144">**Updaters**</span></span>

<span data-ttu-id="1a8dc-145">Monitorare e aggiornare gli utenti per gli aggiornamenti online</span><span class="sxs-lookup"><span data-stu-id="1a8dc-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="1a8dc-146">**Attività di manutenzione**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="1a8dc-147">Tutti gli aggiornamenti devono essere attività di manutenzione, senza alcun requisito di interazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="1a8dc-148">Le app dovrebbero semplicemente aggiornarsi tranquillamente ed eseguire il rollback in caso di errore</span><span class="sxs-lookup"><span data-stu-id="1a8dc-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="1a8dc-149">$ {ROWSPAN2} $**assistenza hardware**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a8dc-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="1a8dc-150">Punti di accesso alternativi</span><span class="sxs-lookup"><span data-stu-id="1a8dc-150">Alternative Access Points</span></span>

<span data-ttu-id="1a8dc-151">Fornire l'accesso alle funzionalità e alle app di Windows accessibili tramite altri punti di accesso in Windows</span><span class="sxs-lookup"><span data-stu-id="1a8dc-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="1a8dc-152">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="1a8dc-153">La chiave consiste nel ridurre le funzionalità duplicate presenti in Windows</span><span class="sxs-lookup"><span data-stu-id="1a8dc-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="1a8dc-154">Notificanti</span><span class="sxs-lookup"><span data-stu-id="1a8dc-154">Notifiers</span></span>

<span data-ttu-id="1a8dc-155">Fornire agli utenti le notifiche relative ai dispositivi</span><span class="sxs-lookup"><span data-stu-id="1a8dc-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="1a8dc-156">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="1a8dc-157">Windows fornisce notifiche agli utenti sui dispositivi</span><span class="sxs-lookup"><span data-stu-id="1a8dc-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="1a8dc-158">**Pre-avviatori**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-158">**Pre-launchers**</span></span>

<span data-ttu-id="1a8dc-159">Alcune attività preliminari richieste dalle app vengono scaricate in un'app di avvio durante l'accesso dell'utente</span><span class="sxs-lookup"><span data-stu-id="1a8dc-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="1a8dc-160">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="1a8dc-161">Windows 8 è ottimizzato per un'esperienza rapida per i lanci di app.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="1a8dc-162">$ {ROWSPAN4} $**Utility**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a8dc-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="1a8dc-163">Sincronizzazione PC</span><span class="sxs-lookup"><span data-stu-id="1a8dc-163">PC Sync</span></span>

<span data-ttu-id="1a8dc-164">Fornire funzionalità di sincronizzazione tra più sistemi</span><span class="sxs-lookup"><span data-stu-id="1a8dc-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="1a8dc-165">**Avvio** (potenziali aggiornamenti nella versione beta)</span><span class="sxs-lookup"><span data-stu-id="1a8dc-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="1a8dc-166">Backup & ripristino</span><span class="sxs-lookup"><span data-stu-id="1a8dc-166">Backup & Recovery</span></span>

<span data-ttu-id="1a8dc-167">Punto di ingresso per salvare e ripristinare lo stato di file, impostazioni o interi sistemi</span><span class="sxs-lookup"><span data-stu-id="1a8dc-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="1a8dc-168">**App di Windows Store per l'interazione con gli utenti**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="1a8dc-169">Telemetria</span><span class="sxs-lookup"><span data-stu-id="1a8dc-169">Telemetry</span></span>

<span data-ttu-id="1a8dc-170">Raccogli e invia informazioni sull'esperienza utente e sull'ambiente</span><span class="sxs-lookup"><span data-stu-id="1a8dc-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="1a8dc-171">**Attività di manutenzione**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-171">**Maintenance Task**</span></span>

<span data-ttu-id="1a8dc-172">Monitoraggio del PC</span><span class="sxs-lookup"><span data-stu-id="1a8dc-172">PC Monitoring</span></span>

<span data-ttu-id="1a8dc-173">Fornire il monitoraggio dello stato del sistema non richiesto e le notifiche che duplicano la funzionalità di posta in arrivo esistente</span><span class="sxs-lookup"><span data-stu-id="1a8dc-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="1a8dc-174">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="1a8dc-175">La chiave consiste nel ridurre le funzionalità duplicate presenti in Windows</span><span class="sxs-lookup"><span data-stu-id="1a8dc-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="1a8dc-176">$ {ROWSPAN2} $**Security**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1a8dc-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="1a8dc-177">Filtri & per il controllo parentale</span><span class="sxs-lookup"><span data-stu-id="1a8dc-177">Parental Control & Filters</span></span>

<span data-ttu-id="1a8dc-178">Applicare le regole e le restrizioni stabilite per l'utilizzo e l'accesso a Internet</span><span class="sxs-lookup"><span data-stu-id="1a8dc-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="1a8dc-179">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-179">**Startup**</span></span>

<span data-ttu-id="1a8dc-180">Configurazione e gestione</span><span class="sxs-lookup"><span data-stu-id="1a8dc-180">Configuration & Management</span></span>

<span data-ttu-id="1a8dc-181">Consenti agli utenti di controllare le opzioni di diagnostica e correzione per il monitoraggio della sicurezza del sistema notificare agli utenti i risultati e le azioni di sicurezza</span><span class="sxs-lookup"><span data-stu-id="1a8dc-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="1a8dc-182">**App di Windows Store per l'interazione con gli utenti**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="1a8dc-183">**Comunicazione & Internet** (im & VoIP)</span><span class="sxs-lookup"><span data-stu-id="1a8dc-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="1a8dc-184">Inviare e ricevere messaggi e chiamate</span><span class="sxs-lookup"><span data-stu-id="1a8dc-184">Send and receive messages and calls</span></span>

<span data-ttu-id="1a8dc-185">**App di Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-185">**Windows Store app**</span></span>

<span data-ttu-id="1a8dc-186">**Music & MP3**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-186">**Music & MP3**</span></span>

<span data-ttu-id="1a8dc-187">Riprodurre, archiviare e gestire musica</span><span class="sxs-lookup"><span data-stu-id="1a8dc-187">Play, store, and manage music</span></span>

<span data-ttu-id="1a8dc-188">**App di Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-188">**Windows Store app**</span></span>

<span data-ttu-id="1a8dc-189">**Video & foto**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-189">**Photo & Video**</span></span>

<span data-ttu-id="1a8dc-190">Rilevare, registrare, eseguire il rendering, archiviare e gestire foto e video</span><span class="sxs-lookup"><span data-stu-id="1a8dc-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="1a8dc-191">**App di Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-191">**Windows Store app**</span></span>

<span data-ttu-id="1a8dc-192">**Giochi per PC**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-192">**PC Gaming**</span></span>

<span data-ttu-id="1a8dc-193">Avviare giochi tra diversi domini</span><span class="sxs-lookup"><span data-stu-id="1a8dc-193">Launch games across various domains</span></span>

<span data-ttu-id="1a8dc-194">**App di Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-194">**Windows Store app**</span></span>

<span data-ttu-id="1a8dc-195">**Annuncio & di vendita**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="1a8dc-196">Attirare l'attenzione sui beni e i servizi disponibili per l'acquisto</span><span class="sxs-lookup"><span data-stu-id="1a8dc-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="1a8dc-197">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="1a8dc-198">Le linee guida sulle app di accessibilità sono coperte da Engagement diretti distinti con gli ISV.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="1a8dc-199">Per informazioni dettagliate, vedere [*programmazione per semplificare l'accesso*](../winauto/ease-of-access---assistive-technology-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8dc-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="1a8dc-200">**App di Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-200">**Windows Store apps**</span></span>

<span data-ttu-id="1a8dc-201">Le app di Windows Store migliorano l'esperienza utente introducendo uno spazio Windows con nuove coordinate: un nuovo modello di app, una nuova interfaccia utente e un Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="1a8dc-202">Queste opzioni relative al linguaggio e al Framework di presentazione sono disponibili per lo sviluppo di app di Windows Store:</span><span class="sxs-lookup"><span data-stu-id="1a8dc-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="1a8dc-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="1a8dc-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="1a8dc-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="1a8dc-204">XAML/C#</span></span>
-   <span data-ttu-id="1a8dc-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="1a8dc-205">XAML/C++</span></span>

<span data-ttu-id="1a8dc-206">Le informazioni aggregate per lo sviluppo di app di Windows Store sono disponibili nel [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="1a8dc-207">Esempi:</span><span class="sxs-lookup"><span data-stu-id="1a8dc-207">Examples:</span></span>

-   <span data-ttu-id="1a8dc-208">[Sviluppo di giochi di Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1a8dc-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="1a8dc-209">[Sviluppo di un'app di Windows Store che usa supporti](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1a8dc-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="1a8dc-210">**Attività di manutenzione automatica**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="1a8dc-211">L'attività in background periodica deve essere progettata come attività di manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="1a8dc-212">Questi sono pianificati al tempo di inattività del sistema per aumentare la velocità di risposta e l'efficienza energetica dei PC Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="1a8dc-213">Le attività di manutenzione possono essere create e configurate da un'applicazione desktop al momento dell'installazione usando desktop SDK.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="1a8dc-214">Per informazioni dettagliate, vedere l'argomento manutenzione automatica che segue.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="1a8dc-215">Risorse</span><span class="sxs-lookup"><span data-stu-id="1a8dc-215">Resources</span></span>

-   [<span data-ttu-id="1a8dc-216">Linee guida sull'accessibilità</span><span class="sxs-lookup"><span data-stu-id="1a8dc-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="1a8dc-217">Windows Dev Center</span><span class="sxs-lookup"><span data-stu-id="1a8dc-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="1a8dc-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1a8dc-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

