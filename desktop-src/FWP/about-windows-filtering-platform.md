---
title: Informazioni sulla piattaforma filtro Windows
description: Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete di Windows XP e Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299809"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="68f57-103">Informazioni sulla piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="68f57-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="68f57-104">Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete di Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="68f57-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="68f57-105">Pam è costituito da un set di hook nello stack di rete e da un motore di filtro che coordina le interazioni dello stack di rete.</span><span class="sxs-lookup"><span data-stu-id="68f57-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="68f57-106">Componenti di WFP</span><span class="sxs-lookup"><span data-stu-id="68f57-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="68f57-107">Motore di filtro</span><span class="sxs-lookup"><span data-stu-id="68f57-107">Filter Engine</span></span>

<span data-ttu-id="68f57-108">Infrastruttura di filtro a più livelli di base, ospitata in modalità kernel e in modalità utente, che sostituisce i più moduli di filtro nel sottosistema di rete Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="68f57-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="68f57-109">Filtra il traffico di rete a qualsiasi livello del sistema su tutti i campi dati che uno shim può fornire.</span><span class="sxs-lookup"><span data-stu-id="68f57-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="68f57-110">Implementa i filtri "callout" richiamando i callout durante la classificazione.</span><span class="sxs-lookup"><span data-stu-id="68f57-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="68f57-111">Restituisce le azioni "Consenti" o "blocca" allo shim che lo ha richiamato per l'imposizione.</span><span class="sxs-lookup"><span data-stu-id="68f57-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="68f57-112">Fornisce l'arbitraggio tra diverse origini dei criteri.</span><span class="sxs-lookup"><span data-stu-id="68f57-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="68f57-113">Ad esempio, determina la priorità quando un'applicazione viene configurata per proteggere il traffico di rete correlato, ma il firewall locale è configurato per impedire il traffico protetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68f57-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="68f57-114">Motore di filtro di base (BFE)</span><span class="sxs-lookup"><span data-stu-id="68f57-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="68f57-115">Servizio che controlla il funzionamento della piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="68f57-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="68f57-116">Esegue le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="68f57-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="68f57-117">Accetta filtri e altre impostazioni di configurazione per la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="68f57-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="68f57-118">Segnala lo stato corrente del sistema, incluse le statistiche.</span><span class="sxs-lookup"><span data-stu-id="68f57-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="68f57-119">Impone il modello di sicurezza per l'accettazione della configurazione nella piattaforma.</span><span class="sxs-lookup"><span data-stu-id="68f57-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="68f57-120">Ad esempio, un amministratore locale può aggiungere filtri, ma gli altri utenti possono visualizzarli.</span><span class="sxs-lookup"><span data-stu-id="68f57-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="68f57-121">Plumbe le impostazioni di configurazione per altri moduli nel sistema.</span><span class="sxs-lookup"><span data-stu-id="68f57-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="68f57-122">Ad esempio, i criteri di negoziazione IPsec passano a moduli di chiavi IKE/AuthIP, i filtri passano al motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="68f57-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="68f57-123">Shim</span><span class="sxs-lookup"><span data-stu-id="68f57-123">Shims</span></span>

<span data-ttu-id="68f57-124">Componenti in modalità kernel che si trovano tra lo stack di rete e il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="68f57-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="68f57-125">Gli shim effettuano la decisione di filtro classificando il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="68f57-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="68f57-126">Di seguito è riportato un elenco di shim disponibili.</span><span class="sxs-lookup"><span data-stu-id="68f57-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="68f57-127">Shim ALE (Application Layer Enforcement).</span><span class="sxs-lookup"><span data-stu-id="68f57-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="68f57-128">Shim del modulo layer di trasporto.</span><span class="sxs-lookup"><span data-stu-id="68f57-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="68f57-129">Shim del modulo a livello di rete.</span><span class="sxs-lookup"><span data-stu-id="68f57-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="68f57-130">Shim di errore Internet Control Message Protocol (ICMP).</span><span class="sxs-lookup"><span data-stu-id="68f57-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="68f57-131">Ignora shim.</span><span class="sxs-lookup"><span data-stu-id="68f57-131">Discard shim.</span></span>
-   <span data-ttu-id="68f57-132">Shim flusso.</span><span class="sxs-lookup"><span data-stu-id="68f57-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="68f57-133">Callout</span><span class="sxs-lookup"><span data-stu-id="68f57-133">Callouts</span></span>

<span data-ttu-id="68f57-134">Set di funzioni esposte da un driver e utilizzate per il filtraggio specializzato.</span><span class="sxs-lookup"><span data-stu-id="68f57-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="68f57-135">Oltre alle azioni di base di "Consenti" e "blocco", i callout possono modificare e proteggere il traffico di rete in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="68f57-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="68f57-136">Per ulteriori informazioni sui callout, vedere l'argomento [driver di callout della piattaforma filtro Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) nella documentazione di Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="68f57-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="68f57-137">PAM fornisce callout predefiniti che eseguono le seguenti attività.</span><span class="sxs-lookup"><span data-stu-id="68f57-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="68f57-138">Eseguire l'elaborazione IPsec.</span><span class="sxs-lookup"><span data-stu-id="68f57-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="68f57-139">Modificare il comportamento del filtro con stato.</span><span class="sxs-lookup"><span data-stu-id="68f57-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="68f57-140">Eseguire il filtro in modalità Stealth (eliminazione invisibile di pacchetti non richiesti).</span><span class="sxs-lookup"><span data-stu-id="68f57-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="68f57-141">Controllare TCP Chimney Offload.</span><span class="sxs-lookup"><span data-stu-id="68f57-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="68f57-142">Interagire con il servizio Teredo.</span><span class="sxs-lookup"><span data-stu-id="68f57-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="68f57-143">Il motore di filtro consente la registrazione di callout di terze parti in ognuno dei relativi livelli in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="68f57-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="68f57-144">Interfaccia di programmazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="68f57-144">Application Programming Interface</span></span>

<span data-ttu-id="68f57-145">Set di tipi di dati e funzioni disponibili agli sviluppatori per compilare e gestire le applicazioni di filtro di rete.</span><span class="sxs-lookup"><span data-stu-id="68f57-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="68f57-146">Questi tipi di dati e funzioni sono raggruppati in più [set di API](api-sets.md).</span><span class="sxs-lookup"><span data-stu-id="68f57-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="68f57-147">Funzionalità di WFP</span><span class="sxs-lookup"><span data-stu-id="68f57-147">WFP Features</span></span>

-   <span data-ttu-id="68f57-148">Fornisce un'infrastruttura di filtro dei pacchetti in cui i fornitori di software indipendenti (ISV) possono collegare moduli di filtro specializzati.</span><span class="sxs-lookup"><span data-stu-id="68f57-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="68f57-149">Funziona con IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="68f57-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="68f57-150">Consente il filtraggio, la modifica e il reinserimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="68f57-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="68f57-151">Esegue l'elaborazione di pacchetti e flussi.</span><span class="sxs-lookup"><span data-stu-id="68f57-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="68f57-152">Consente l'abilitazione del filtro pacchetti per ogni applicazione, per utente e per connessione, oltre a per interfaccia di rete o per porta.</span><span class="sxs-lookup"><span data-stu-id="68f57-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="68f57-153">Fornisce la sicurezza in fase di avvio fino a quando non è possibile avviare BFE (Base Filtering Engine).</span><span class="sxs-lookup"><span data-stu-id="68f57-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="68f57-154">Consente di filtrare le connessioni con stato.</span><span class="sxs-lookup"><span data-stu-id="68f57-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="68f57-155">Gestisce sia i dati pre che quelli crittografati tramite IPsec.</span><span class="sxs-lookup"><span data-stu-id="68f57-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="68f57-156">Consente l'integrazione dei criteri di filtro firewall e IPsec.</span><span class="sxs-lookup"><span data-stu-id="68f57-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="68f57-157">Fornisce un'infrastruttura di gestione dei criteri per determinare quando devono essere attivati filtri specifici.</span><span class="sxs-lookup"><span data-stu-id="68f57-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="68f57-158">Ciò include la mediazione dei requisiti in conflitto da più filtri forniti da fornitori diversi.</span><span class="sxs-lookup"><span data-stu-id="68f57-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="68f57-159">Gestisce la maggior parte del riassemblaggio del pacchetto e del rilevamento dello stato.</span><span class="sxs-lookup"><span data-stu-id="68f57-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="68f57-160">Include un sistema di notifica utente generico che informa i sottoscrittori delle modifiche apportate al sistema di filtraggio.</span><span class="sxs-lookup"><span data-stu-id="68f57-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="68f57-161">Implementa funzioni di enumerazione che segnalano lo stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="68f57-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="68f57-162">USA gli eventi NET per registrare gli errori IPsec e le gocce di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="68f57-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="68f57-163">Supporta una [classe helper NDF (](/windows/desktop/NDF/extensible-helper-classes)Network Diagnostics Framework).</span><span class="sxs-lookup"><span data-stu-id="68f57-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="68f57-164">Supporta le [estensioni Secure Socket](/windows/desktop/WinSock/winsock-secure-socket-extensions) per l'API Winsock, che consentono alle applicazioni di rete di proteggere il traffico tramite la configurazione di WFP.</span><span class="sxs-lookup"><span data-stu-id="68f57-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="68f57-165">Ai livelli dell'applicazione a livello di applicazione (ALE), ha un effetto minimo sulle prestazioni di rete mediante l'elaborazione del primo pacchetto in una connessione.</span><span class="sxs-lookup"><span data-stu-id="68f57-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="68f57-166">Integra l'offload hardware in cui i moduli di callout in modalità kernel possono usare l'hardware per eseguire un'ispezione specifica dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="68f57-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68f57-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68f57-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68f57-168">Architettura WFP</span><span class="sxs-lookup"><span data-stu-id="68f57-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="68f57-169">Operazione PAM</span><span class="sxs-lookup"><span data-stu-id="68f57-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="68f57-170">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="68f57-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="68f57-171">Configurazione IPsec</span><span class="sxs-lookup"><span data-stu-id="68f57-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="68f57-172">Configurazione di WFP</span><span class="sxs-lookup"><span data-stu-id="68f57-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="68f57-173">Monitoraggio WFP</span><span class="sxs-lookup"><span data-stu-id="68f57-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="68f57-174">API PAM</span><span class="sxs-lookup"><span data-stu-id="68f57-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

